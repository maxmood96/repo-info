## `gradle:8-jdk23-corretto-al2023`

```console
$ docker pull gradle@sha256:f88a86f2f6a5c9b6dbd4dc4213f9701cd2b139f59cc7168fefa4bdc82cd97f4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk23-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:4b9fea62ef117443cd522757d0edde4852480777ffcf52998e6e685d9d06ac1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.6 MB (439629666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38fdac02f11032563223bf0d544450b9803801da5f1f83d58924fcd5831bda47`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Wed, 19 Feb 2025 02:55:56 GMT
CMD ["gradle"]
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 19 Feb 2025 02:55:56 GMT
WORKDIR /home/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_VERSION=8.12.1
# Wed, 19 Feb 2025 02:55:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
USER gradle
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
USER root
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b7af05e057fd5e223e72a7d86db6ccf9a1448d643657ef1e37b69605210c97`  
		Last Modified: Thu, 27 Feb 2025 21:08:47 GMT  
		Size: 177.6 MB (177592724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0873c197fa52e7ce85571956337a00209ea9cae9d875ad7461adcb008e52d9e6`  
		Last Modified: Thu, 27 Feb 2025 22:09:10 GMT  
		Size: 72.3 MB (72266705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00edd742b77425ae4e29c06ddbc1aebe6245b0465e6b74a655dc3162189c03f5`  
		Last Modified: Thu, 27 Feb 2025 22:09:07 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08efe248fff9ce6aaa23fbb4e6c181f34fd39e6dfeb847624b545e19fcd13e6f`  
		Last Modified: Thu, 27 Feb 2025 22:09:11 GMT  
		Size: 136.6 MB (136561922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd362073898666a0e822e3525fc311d5c415c732c3a9af5940aa28e18bc1cbb`  
		Last Modified: Thu, 27 Feb 2025 22:09:08 GMT  
		Size: 54.9 KB (54903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:f2b42fc47bee651bd3f3efe00c8fa1e07979d4c419c941678c09fb25b7020d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10762345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb4c5fd2c259bc17e68ecfbedc9f4a809f6fe6b201db67967cf6fcd55e401a1`

```dockerfile
```

-	Layers:
	-	`sha256:4a248986f4969b7d1781835c127d4cf0fc480f3ec7dd52cac51a3822a51ec04a`  
		Last Modified: Thu, 27 Feb 2025 22:09:08 GMT  
		Size: 10.7 MB (10742436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8688c1e069a678881ca8800f4ac7766bebe89055cca47ff8af202cd94dfd86b6`  
		Last Modified: Thu, 27 Feb 2025 22:09:07 GMT  
		Size: 19.9 KB (19909 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk23-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:923df9f8ebe1b1f094c7781276fb6a71fd1158550ef7da5b00f5dfd0f2e01390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.5 MB (436464998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:324de771ae79a1efe6fe1c5455e044e9c36056565e058cf62583d89382f7e9ea`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Wed, 19 Feb 2025 02:55:56 GMT
CMD ["gradle"]
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 19 Feb 2025 02:55:56 GMT
WORKDIR /home/gradle
# Wed, 19 Feb 2025 02:55:56 GMT
ENV GRADLE_VERSION=8.12.1
# Wed, 19 Feb 2025 02:55:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
USER gradle
# Wed, 19 Feb 2025 02:55:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8d97a97984f6cbd2b85fe4c60a743440a347544bf18818048e611f5288d46c94
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 19 Feb 2025 02:55:56 GMT
USER root
```

-	Layers:
	-	`sha256:ae97a46dbe642672a09bd4ab6df7280b70a40f641ef4a637aa82879145ebcb67`  
		Last Modified: Sat, 22 Feb 2025 01:44:42 GMT  
		Size: 52.3 MB (52271270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54469013ccf794077e3663cbfeb27227feeda108f7a6a129eaac54867444c07b`  
		Last Modified: Thu, 27 Feb 2025 21:24:55 GMT  
		Size: 175.6 MB (175622009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaa757ea179d1f205616331b5ea0d3a5b3641551b000a9e1fff4831ec367b3d`  
		Last Modified: Thu, 27 Feb 2025 22:12:57 GMT  
		Size: 71.9 MB (71948587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba28f9ae8e12c64059b2fd115bf6da36c8a39a9aaaddf52499f67a44ccb968f`  
		Last Modified: Thu, 27 Feb 2025 22:12:54 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee45d46d3362e3bdfa065349cf44cee34a607ca60971cea35f2144f8babc0bf`  
		Last Modified: Thu, 27 Feb 2025 22:12:58 GMT  
		Size: 136.6 MB (136561923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9878016efff31b3a7d6b3ea4da0a77a8ce2048d81b8139afdba2ad79947a1`  
		Last Modified: Thu, 27 Feb 2025 22:12:54 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:15553a7e6d20704b04cedbb9002bd4dad4ce4cdcfebb263fe76651f1268a6174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10760731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ec64dcab1c2d60db118f20cb98a191fa9df513f9b31b45c42be863c977957c`

```dockerfile
```

-	Layers:
	-	`sha256:7db8d9160ced30e9636af7ff3b02c471742e3f96aa88841fd5e9810fcbc5b2a6`  
		Last Modified: Thu, 27 Feb 2025 22:12:55 GMT  
		Size: 10.7 MB (10740625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48fc7e7b77113e5cc05b98cafefcdf9fb10a6261466765b830ccf9060d8f2b28`  
		Last Modified: Thu, 27 Feb 2025 22:12:54 GMT  
		Size: 20.1 KB (20106 bytes)  
		MIME: application/vnd.in-toto+json
