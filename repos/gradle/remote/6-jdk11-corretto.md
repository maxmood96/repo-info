## `gradle:6-jdk11-corretto`

```console
$ docker pull gradle@sha256:12fd336c4b6dcc3180919607fe92b0c290dc91256a1b9d2e9a063ef103fa49b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:1d87ae68c9c3cfa5af710f5011f0a1387f24e6e52d8d8d2e1943c803f9ac178a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.3 MB (402348059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f6da6bf80ad304ff0bb962a0a9d1af3b4231b74a86c7202ddc4ff861517e64`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:45 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:45 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:45 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 04 May 2026 20:42:53 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:53 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:53 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:53 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 04 May 2026 20:42:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 04 May 2026 20:42:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:56 GMT
USER gradle
# Mon, 04 May 2026 20:42:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:56 GMT
USER root
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177f5f6694b7a14aaccd527d192e8e76c94dfecbb9fdd2f8693b660e84198ec2`  
		Last Modified: Mon, 04 May 2026 20:12:07 GMT  
		Size: 153.5 MB (153472514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef425309678952c294727da7e41d41e0d00b6775f0e12208ea9faef2f97aaae4`  
		Last Modified: Mon, 04 May 2026 20:43:24 GMT  
		Size: 86.2 MB (86169173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c3959efff21a31a8ceb7a70ce51c6b806e0120e9d81d390f66ec40cc0eb863`  
		Last Modified: Mon, 04 May 2026 20:43:21 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ff6ba214b36e251ba3504931ed94a185642fec2a2a86f1ba1bdbcb0a1033d5`  
		Last Modified: Mon, 04 May 2026 20:43:25 GMT  
		Size: 107.7 MB (107696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0ca6a2b360fb269f1a8ffbf05728b26000511290faed0d79c65a4bada9c392`  
		Last Modified: Mon, 04 May 2026 20:43:21 GMT  
		Size: 431.3 KB (431276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c4844c3a37f76c496f34456393649cdc2ca849288f94a3ef506961483c6c31db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11288649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9521a60e9e24cb309b063a78d807ea68d61964e8238c5b3d2f64dace500ed0c`

```dockerfile
```

-	Layers:
	-	`sha256:42c029c1f84ef9e371ef4a2f4764d54fdb43a4a5fea9a578c6f77aaa02fc18fb`  
		Last Modified: Mon, 04 May 2026 20:43:21 GMT  
		Size: 11.3 MB (11267778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33dc98294fb63281cecd0b416304b912e8087cf6f0fc0b7b1613c9c9c44c4cb5`  
		Last Modified: Mon, 04 May 2026 20:43:21 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c2097970703606e8ecb076b8cca028c82a27299bf7a6a893ea23edbd99372fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399289287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a7e915ee8778832c4c14fc032f1e0d51cb09022927e0cd1c46f6358f5dd130`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:32 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:32 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:32 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 04 May 2026 20:42:55 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:55 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:55 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:55 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:55 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:55 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:55 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 04 May 2026 20:42:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 04 May 2026 20:42:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:58 GMT
USER gradle
# Mon, 04 May 2026 20:42:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:58 GMT
USER root
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838136ec5b6ab2b88d9936cfc6ef1491350d124ec8e540cec804c91561010d10`  
		Last Modified: Mon, 04 May 2026 20:11:53 GMT  
		Size: 152.1 MB (152051592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fedf2c32fd2d77eba69e15016d7756b29076690006d182be7274e7ca2165a2`  
		Last Modified: Mon, 04 May 2026 20:43:29 GMT  
		Size: 85.7 MB (85657555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b89311c38127a2ae3a03f53f54a98a00b794cb0c013245115173f1b96bd325`  
		Last Modified: Mon, 04 May 2026 20:43:25 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bdb6c4a4676ed6229cfcfe699f1e1e5e9dc6efee06998a4ea36446fcc0f7b9`  
		Last Modified: Mon, 04 May 2026 20:43:30 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faff0f6682d3292af5acf61e6dd2a292a9f8f37f5e6f3349855adbbc512481c3`  
		Last Modified: Mon, 04 May 2026 20:43:26 GMT  
		Size: 425.0 KB (425027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a202bf457b0b36ba1af2e4e9e7ad52f854193d1c8419c5ba9c49e72240371b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11288642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7832784257d49765c08499a037bff75d28f864f3af9bb6681bd5a8041d91b1ad`

```dockerfile
```

-	Layers:
	-	`sha256:97a9e00e44889efcbaf0a12c361ff5d354e3d5cf2951377dfb000c539a5c4bd0`  
		Last Modified: Mon, 04 May 2026 20:43:26 GMT  
		Size: 11.3 MB (11267597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e47d9ef39c4fa8c073b3f548a516442630fd5351fe2388a5cf55a7395b26a8d4`  
		Last Modified: Mon, 04 May 2026 20:43:26 GMT  
		Size: 21.0 KB (21045 bytes)  
		MIME: application/vnd.in-toto+json
