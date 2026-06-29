## `gradle:9-jdk25-corretto`

```console
$ docker pull gradle@sha256:a0e569b4397e58370fc20f48fa770c7c63b9d0db3ce4d8df5f84f02a6b74ab54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:6af5bbff23e8aa3d804895a25515c21c140c6196402c260715857552f121a2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.3 MB (471257443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3dde7497229bec9de7ceb05f68def3552d5c1662482a3dd3586127a194db2f`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:15 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:05:15 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:15 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:15 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 29 Jun 2026 17:11:44 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:11:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:11:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:11:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:11:44 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:11:44 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:11:44 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:11:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:11:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:11:47 GMT
USER gradle
# Mon, 29 Jun 2026 17:11:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:11:48 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9187d1c0652a3fc2e5587c51e615fc4dcfb4ee369050a626cc0c5f8763605ac`  
		Last Modified: Mon, 22 Jun 2026 18:05:41 GMT  
		Size: 189.4 MB (189413466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8232024d4f87e9eaf039dbcef58a654f09f5bc51242e7a829f3a1d84edd930fd`  
		Last Modified: Mon, 29 Jun 2026 17:12:20 GMT  
		Size: 86.6 MB (86646460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf906ed39c5adfe23766fbeb1bac52480dec6c0cc5de35879c7c9f99544479b`  
		Last Modified: Mon, 29 Jun 2026 17:12:17 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4e3ec652be4e1ce82154c178e092666788a877c3d4e602b11979047fe85b3d`  
		Last Modified: Mon, 29 Jun 2026 17:12:21 GMT  
		Size: 140.6 MB (140596023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654e01ffd83ae16a48e41dabe94e729ad29d79196baa8cd711cd62d82a370a21`  
		Last Modified: Mon, 29 Jun 2026 17:12:17 GMT  
		Size: 25.6 KB (25632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:5fd6e786a18164d87d4f606b4c1d21832e7500aeeb4781ac05f5a0d357851d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11419497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7170298695b04798b4a21a206a4573d7cb1b328936589ee8757dbf3d4ca643cf`

```dockerfile
```

-	Layers:
	-	`sha256:c7885dc4e26ab39ab0f70ac390d1b07b7637c9eb57d85e37e4f5067bb17aeb8e`  
		Last Modified: Mon, 29 Jun 2026 17:12:18 GMT  
		Size: 11.4 MB (11397228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:343619c08cb80f869a412a8d4c26826d1e0607079bce3615c4d01beeca6af4fb`  
		Last Modified: Mon, 29 Jun 2026 17:12:17 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:1cfa4b0d2ff60a2c700e69ab1ae850223e610c06e6c12ee753a1f0ca00c9f737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.4 MB (467443311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61862252b358e4a37cb37f47e0b5a3bd66d8bde1e85355f61f6736803d023295`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:33 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:15:33 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:33 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:33 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 29 Jun 2026 17:11:46 GMT
CMD ["gradle"]
# Mon, 29 Jun 2026 17:11:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Jun 2026 17:11:46 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Jun 2026 17:11:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Jun 2026 17:11:46 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Jun 2026 17:11:46 GMT
WORKDIR /home/gradle
# Mon, 29 Jun 2026 17:11:46 GMT
ENV GRADLE_VERSION=9.6.1
# Mon, 29 Jun 2026 17:11:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
# Mon, 29 Jun 2026 17:11:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Jun 2026 17:11:49 GMT
USER gradle
# Mon, 29 Jun 2026 17:11:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9c0f7faeeb306cb14e4279a3e084ca6b596894089a0638e68a07c945a32c9e14
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 29 Jun 2026 17:11:50 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4f1006a54abcd81b4b8010a4470cc0f1ddc33b2dd4191d1661555e3275be62`  
		Last Modified: Mon, 22 Jun 2026 18:15:59 GMT  
		Size: 187.3 MB (187328296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88314328a72c286073e07e421cc20102a23cbd7c1446d90df4ff17c79a3a9a1e`  
		Last Modified: Mon, 29 Jun 2026 17:12:23 GMT  
		Size: 86.0 MB (86037277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554549e3c51dcf241bcb350be35be553f834b96519a5562f7fb78ca284bbd803`  
		Last Modified: Mon, 29 Jun 2026 17:12:19 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d66ef5a8ddaabada5e357ec1791102800d6cba0eb85ca3a5cd183239845f056`  
		Last Modified: Mon, 29 Jun 2026 17:12:24 GMT  
		Size: 140.6 MB (140596026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19451c1f85841b1d588f2dd0038eb668fea3e977f6322d494a713df5a28b6eb`  
		Last Modified: Mon, 29 Jun 2026 17:12:19 GMT  
		Size: 29.3 KB (29347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:8b6d957eda25f91f4396362758737babd210124a1e19f44a1bf22a24767f3baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11418756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544efc55acc12f4b13ed392e27003cfb80bbe30eea9d6cc8cbf1df3fc8142acb`

```dockerfile
```

-	Layers:
	-	`sha256:1a58d7fe1a582a5c4f300eac8828ddf12eb8320924857866b7fbad47cb189533`  
		Last Modified: Mon, 29 Jun 2026 17:12:20 GMT  
		Size: 11.4 MB (11396266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:544025c84b3f7c2a6c12b1a72ab78117ff2a796ed820a0e599b4b85c25402fec`  
		Last Modified: Mon, 29 Jun 2026 17:12:19 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
