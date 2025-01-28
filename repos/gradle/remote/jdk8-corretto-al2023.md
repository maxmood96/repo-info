## `gradle:jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:8ca1314be0e5c3c052a1d5c2e846691f1a4b9e5c33a547bff6d0e58e63f25ab1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:328686f5f912da96fed4d01ac801e00e9fe558c65e6a590f23799071670a109a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.1 MB (525071981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a0d5acf1da23eb8ee4e7a089cf7e5cc85036313e20580fcced68e35d65eb98`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:40 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=1.8.0_442.b06-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["gradle"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 27 Jan 2025 19:22:41 GMT
WORKDIR /home/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_VERSION=8.12.1
# Mon, 27 Jan 2025 19:22:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER gradle
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER root
```

-	Layers:
	-	`sha256:fa97b7596fdd91f8ccf1ccf8ee7189f9449877cc795e39ad814638444b666c80`  
		Last Modified: Fri, 17 Jan 2025 02:00:45 GMT  
		Size: 53.2 MB (53152535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237ec7527849ec87d8ee6ed23ac5bc7da783e7704ba9a980ec6b329315c4dd5b`  
		Last Modified: Thu, 23 Jan 2025 23:08:52 GMT  
		Size: 285.7 MB (285709076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1055c376f2acbb51860d19f2d4321afb443116941493fb07e059f674ef17a8`  
		Last Modified: Tue, 28 Jan 2025 01:28:59 GMT  
		Size: 49.6 MB (49591837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c001d02df5d57825b668b2f84647fd93a8a5d3ccec48cf8277d70e5a0768a4b`  
		Last Modified: Tue, 28 Jan 2025 01:28:58 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3806e0cc367efc3d71e7c10b09d4a86c599135f4aea6802efa2ddd09398438`  
		Last Modified: Tue, 28 Jan 2025 01:29:01 GMT  
		Size: 136.6 MB (136561941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2e089fc86486a55d572f1ae044d147b253c9a93688d6c78310ac768c228b21`  
		Last Modified: Tue, 28 Jan 2025 01:28:58 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:3318fce6878a05f758cd72ea0315bf86d7661d5e2b3758dd651b6bcf38fe16ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16439190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5b1c07ff6909039df5be4d597694ff097c327b85ed6cf4ee606694da4ff016`

```dockerfile
```

-	Layers:
	-	`sha256:afa1672691aac1a1e012b8f9d67d01c12916203ec3aa97b76c54cc7c7b7d12a9`  
		Last Modified: Tue, 28 Jan 2025 01:28:59 GMT  
		Size: 16.4 MB (16419293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baaa517c68debd0732e713dd57a4703349da6ec614f18320d7dd008e6b3e7bef`  
		Last Modified: Tue, 28 Jan 2025 01:28:58 GMT  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f3d1600f04b374febb52bc45ce4debc44665c7dc666e28a08adf9f3959d0344d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.9 MB (377931803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:549f8998c58f96eaf1fe9ddebb7a85b15af83b7475797477108fe5467547e3e0`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:44 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:44 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=1.8.0_442.b06-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 27 Jan 2025 19:22:41 GMT
CMD ["gradle"]
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 27 Jan 2025 19:22:41 GMT
WORKDIR /home/gradle
# Mon, 27 Jan 2025 19:22:41 GMT
ENV GRADLE_VERSION=8.12.1
# Mon, 27 Jan 2025 19:22:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER gradle
# Mon, 27 Jan 2025 19:22:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 27 Jan 2025 19:22:41 GMT
USER root
```

-	Layers:
	-	`sha256:23c58bc83b4b2c70780808282eab12c25cdbe212cc6fa4cd0d9a4d82b1cbf7ce`  
		Last Modified: Fri, 17 Jan 2025 02:10:39 GMT  
		Size: 52.3 MB (52270199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c79836f3f3aca30ae229b87e6ef3a920ce070f8fa90da48d954f5af38a5c8f2`  
		Last Modified: Thu, 23 Jan 2025 23:08:41 GMT  
		Size: 118.7 MB (118697143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ecc39daf4792631a1d9ddbb09d582cb3b8ef26608bc765caf1629b0f2ae30b`  
		Last Modified: Fri, 24 Jan 2025 00:08:26 GMT  
		Size: 70.3 MB (70341299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf70968128045d5adbb646ebaee11e2b424a6c2d8fa635ffc3a044856bfc2e7`  
		Last Modified: Fri, 24 Jan 2025 00:08:23 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693623da0c9ee711f06c324f8e83e03da069c0a9c8b6aac93596984afc8c9c3f`  
		Last Modified: Tue, 28 Jan 2025 01:54:32 GMT  
		Size: 136.6 MB (136561941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba63714f38eb630e1c1f63505df1ebd9134ac5e6a55c72eb27ffd59e44b667c`  
		Last Modified: Tue, 28 Jan 2025 01:54:29 GMT  
		Size: 59.5 KB (59542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:cdab3457422e6dafd7102aafe0e6bf7c74c30ba02b06ac8941e1ae66d587c973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11116492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5561e023bb3563322c8554d15686325c4242d93ccccbcd2c59e72e2c982afca`

```dockerfile
```

-	Layers:
	-	`sha256:68617c0871b774ef4d9bdf6b88b634a23deb5eadc5040899dbb9c935731525f9`  
		Last Modified: Tue, 28 Jan 2025 01:54:29 GMT  
		Size: 11.1 MB (11096397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1b30ddf523d9f43b87134c5b31e07553283bb66a1a61b54078d85cc4b1156e7`  
		Last Modified: Tue, 28 Jan 2025 01:54:28 GMT  
		Size: 20.1 KB (20095 bytes)  
		MIME: application/vnd.in-toto+json
