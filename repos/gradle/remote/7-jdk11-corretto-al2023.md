## `gradle:7-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:1b38013ce3e8be69d7c24325e57e6c63fddf3dd2630186c73748336a7d43d59f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:6b533ee91be4b586027917e86324141a633c26fe7601922e6e26c2231ede76f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.9 MB (401937577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2257f8695c36e0aa51dc5524e85133d1f23004b5248f8834dcf1ff63b9364961`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 18 Feb 2025 21:10:40 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:40 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 18 Feb 2025 21:10:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
USER root
```

-	Layers:
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18fee258c5afc43bce8ea50ba3cfd81555b4302fb52b9b93593c34885372091`  
		Last Modified: Mon, 10 Feb 2025 20:08:48 GMT  
		Size: 153.9 MB (153881573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746bab89b5dc1775f7e6737e6a76b000500d6abdcb7e4a27bf9668674af6a943`  
		Last Modified: Wed, 19 Feb 2025 21:30:47 GMT  
		Size: 72.1 MB (72118308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54267a1da3e542e0947213ea67925a12b88c43d17d3a6c21ff98eb515fb8d655`  
		Last Modified: Wed, 19 Feb 2025 21:30:44 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa061a25c1ad79caa13196231736675c76937faf42bc09c45c9f99c8bdeeab4`  
		Last Modified: Wed, 19 Feb 2025 21:30:48 GMT  
		Size: 122.7 MB (122730525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ace1c14c724735955a4f675d0726cf2ab1bb3bc0b2659bd27dc9b73c358a9c`  
		Last Modified: Wed, 19 Feb 2025 21:30:45 GMT  
		Size: 54.9 KB (54909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:49cc735a008ec8b720a3dcdb8d22454381beb8e0f39f7bf41e0fed1a17cb5722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10694100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49efe8ce9c2bfb62c6782a40c3fb9991ee526577b2bcd5fddacfd1700335847`

```dockerfile
```

-	Layers:
	-	`sha256:76d78f12bc7abeffdfacf34b99263859b46f613ef0bae2b5fc0a22b8e344edc0`  
		Last Modified: Wed, 19 Feb 2025 21:30:45 GMT  
		Size: 10.7 MB (10674847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:266a61744d4cc6d07a5036aa4722371b57912e4e8fbd3f619d799375783c9f59`  
		Last Modified: Wed, 19 Feb 2025 21:30:44 GMT  
		Size: 19.3 KB (19253 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6f57c3ab7032a2e250a9ecdea9996af6a2fdc4462b7917b9f9461de32df7f557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.2 MB (399223910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4153749e03968a158468bee70c875fe80c352e98199e82c8125d47388533e68e`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 18 Feb 2025 21:10:40 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:40 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 18 Feb 2025 21:10:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
USER gradle
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
USER root
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205f238aedf3e4060eccc0ba776c3c96abebc30419939e2ca916d83a4a887793`  
		Last Modified: Mon, 10 Feb 2025 20:16:03 GMT  
		Size: 152.4 MB (152373544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6982eeac1e4df5e46e221ea0c407f44e0d09e6011bb8ac0d45ea6f5d371f1561`  
		Last Modified: Mon, 10 Feb 2025 21:09:57 GMT  
		Size: 71.8 MB (71787683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eff6da54410f575b0fa3a2e7d64e273419db0352d1376ac98212b37d5ae529`  
		Last Modified: Mon, 10 Feb 2025 21:09:55 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e9c2c4e520a1acc966fc6d1cd7d75022890f03d6db1bc417095856e3ec2773`  
		Last Modified: Wed, 19 Feb 2025 22:20:51 GMT  
		Size: 122.7 MB (122730525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc2ce7dea402805f441dc61823e10294ff03faedf291552db4de9adc7c5e83f`  
		Last Modified: Wed, 19 Feb 2025 22:20:48 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a42702f2b08c9dcfc76c280306390f93d5f75be880af5cefbb0bc9f1814fcb09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10694090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4060c2556dd22c119f0d58baa11ceaa9d11c5f012b35722776caa36fe410097a`

```dockerfile
```

-	Layers:
	-	`sha256:e916208a58132f2718aed7cb3c44a2ebc81d5cf87062bf8009be97158b375ec5`  
		Last Modified: Wed, 19 Feb 2025 22:20:48 GMT  
		Size: 10.7 MB (10674666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01dc121f0cbb56453b3301f2fac17567e1d96d67c705c93e6a47e00d5369f0b5`  
		Last Modified: Wed, 19 Feb 2025 22:20:47 GMT  
		Size: 19.4 KB (19424 bytes)  
		MIME: application/vnd.in-toto+json
