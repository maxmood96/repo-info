## `gradle:jdk8-corretto`

```console
$ docker pull gradle@sha256:da03ffa8f6540ccc9f13b657de718c8b14acb6e9cfb918c4661e0b8318423e12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:34e596f3a55bd7661b47ae60d055f7ced0f5edfb7b37dc5f591981673a6922fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.7 MB (526719899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f77d69b20d2e5cbc3ad420f748667d9d1d03a5472a4a9719b8c312fa158caa2`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:cd0d74ad3e8df9e12e36add47213ce9709dfa1360f25ab6f04b201fe34a6fc5a`  
		Last Modified: Thu, 27 Feb 2025 21:08:48 GMT  
		Size: 285.7 MB (285716080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0531e7815143743b42574b90f134e01ce9a18789fdf860987c765d9013f1eca`  
		Last Modified: Thu, 27 Feb 2025 22:09:08 GMT  
		Size: 51.2 MB (51233548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518974ce944903838adb2031521fedd5233050dccdc2ff679a6466a0304d7275`  
		Last Modified: Thu, 27 Feb 2025 22:09:07 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861eaf190ab8ffac69ee536a6f10cfabc25f782be5c7949bac58e24c2cf89425`  
		Last Modified: Thu, 27 Feb 2025 22:09:10 GMT  
		Size: 136.6 MB (136561942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e0bb184db59e8370b36712e41f92cd096c72b00d7697bcc3de52bf8bad9f8c`  
		Last Modified: Thu, 27 Feb 2025 22:09:08 GMT  
		Size: 54.9 KB (54912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:58e30cfa4d9388b7e0af6ebf0513b437e8a645b076b0385a1025cfff70413ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16458256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9e186ffe9f5b4090cf47071b94dc6c605a643c2149ddc141eb5596c57db998`

```dockerfile
```

-	Layers:
	-	`sha256:ae150d55b14b7a79c0400d707ea9c0fb2cd1d58e846e72db8d557efccccdce76`  
		Last Modified: Thu, 27 Feb 2025 22:09:08 GMT  
		Size: 16.4 MB (16438358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b399402b48ddd6274c01b627043c2112926469ce4f1ef24bf6d5142442add78`  
		Last Modified: Thu, 27 Feb 2025 22:09:07 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:26e104df915aca7641b7b3f0688dacfc00f98b132903c30159e460e1601539c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.5 MB (379538174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8d2545f2f5a441997e9274ead6a5d0cb5f9b5d3d17280ebd0721a6cf60b238`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:c61a9092db6a68cb29f86b49e0b007c27dc9e26cbf6be2064652161b836c563d`  
		Last Modified: Thu, 27 Feb 2025 21:08:38 GMT  
		Size: 118.7 MB (118712044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d632256f4534e6a2ef91336826d966c1048b6a6c8ef011507eb315af61e6bb`  
		Last Modified: Thu, 27 Feb 2025 22:11:45 GMT  
		Size: 71.9 MB (71931709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139c5fc6e4499972051ba2ab6b7c726dc2bce7d7da13dc2d9582eb7a0e1c4bf3`  
		Last Modified: Thu, 27 Feb 2025 22:11:42 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf262b0aec496fec04b91e8d3dd2b90c8da54cefca05ce2da91863618c49ccf9`  
		Last Modified: Thu, 27 Feb 2025 22:11:48 GMT  
		Size: 136.6 MB (136561940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b3165ba056ddc24aa671c788219e64e7028e2292a624f663d8a2fa729c72bc9`  
		Last Modified: Thu, 27 Feb 2025 22:11:43 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:5ca619d38043792c73558d0337ffaa61b04c4fad983f3f2e1fe109646187ba66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11135557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5a30a2bb452cfbb5dfe232ce04043cb075b5788e9f0124d1173b8a79a83fbe`

```dockerfile
```

-	Layers:
	-	`sha256:87b146ab8ff05510d52f27a56ec7883152ade9222c72ff831da1f0af982779ce`  
		Last Modified: Thu, 27 Feb 2025 22:11:43 GMT  
		Size: 11.1 MB (11115462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb87181976c4b81999f25ea3653c5a5cd45672ef5e31c5edc33f5c2ba33ab14d`  
		Last Modified: Thu, 27 Feb 2025 22:11:42 GMT  
		Size: 20.1 KB (20095 bytes)  
		MIME: application/vnd.in-toto+json
