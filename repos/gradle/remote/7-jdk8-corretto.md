## `gradle:7-jdk8-corretto`

```console
$ docker pull gradle@sha256:8215cedcbbc2bc5cac89fd905e53722682b6feaebd478812e3179eccc5423528
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:b9f02b20fa3282e318d6499ac5721f48baba469e771ea1276760eeef3def649c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578847564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806628cbb8649951ef5df34da698c9f9b7022d3b1454162a5c5f94cca8c1fe74`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:09 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:59:09 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:09 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 21 Jan 2026 19:17:51 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:17:51 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:17:51 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:17:51 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:17:51 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:17:51 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:17:51 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 21 Jan 2026 19:17:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 21 Jan 2026 19:17:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:17:53 GMT
USER gradle
# Wed, 21 Jan 2026 19:17:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 21 Jan 2026 19:17:54 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4054be9abe76295ab4b3be753153a92dc7373aff9dabca474c7604a429b63c`  
		Last Modified: Wed, 21 Jan 2026 19:00:00 GMT  
		Size: 330.9 MB (330929043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2381eb0ae6bb1405d813136f04b27fa8cf34736ef8462342d65a7809cf0857`  
		Last Modified: Wed, 21 Jan 2026 19:18:56 GMT  
		Size: 65.4 MB (65371016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d3543e5b664ac5ef95b72eada1d15413b89a8697262982ef51cd9e3e4462d`  
		Last Modified: Wed, 21 Jan 2026 22:13:37 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f300f5fe869f26bd41a0ab1ff29ae495781dcf0a5dcf94c78a584092c610887`  
		Last Modified: Wed, 21 Jan 2026 19:18:33 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d36de1ebab03c4fb7799541ec27ee9604f7deb4a54b75881f7fe4ef9bf43a1a`  
		Last Modified: Wed, 21 Jan 2026 19:18:29 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:82c516f20c776d2cf275d6851d66b801dad0d890f68f14e1790fc9320965ead4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18084720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ac821529d1e319365cff808d469b8862f86e68e9ae4a5d6afc641c0d3b4c31`

```dockerfile
```

-	Layers:
	-	`sha256:fd9c80e98651dc03cc4189664d5db691ff8a717005f3521606d1867198d9b215`  
		Last Modified: Wed, 21 Jan 2026 19:18:30 GMT  
		Size: 18.1 MB (18063856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bfaced8313b6f348bdfa6094053db1900c2936b4d85a2a290a85a0dcb13d666`  
		Last Modified: Wed, 21 Jan 2026 21:19:14 GMT  
		Size: 20.9 KB (20864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:40a81f0231b7e2290355e0f4fb12b5ac898ed5ca149eb46fa269ab8d54a39701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384910647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5717ffbed895b2de4abe6034f87b74ac5ca505e97d7f853f9ea907f3fefcb12f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:28 GMT
ARG version=1.8.0_482.b08-1
# Wed, 21 Jan 2026 18:59:28 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:28 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 21 Jan 2026 19:16:33 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:16:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:16:33 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:16:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:16:33 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:16:33 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:16:33 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 21 Jan 2026 19:16:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 21 Jan 2026 19:17:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:17:36 GMT
USER gradle
# Wed, 21 Jan 2026 19:17:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 21 Jan 2026 19:17:37 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e639ecdb26d59a37e73ea4a155c69ad55efad10cc4eec6c6e84f5e19ac8fff`  
		Last Modified: Wed, 21 Jan 2026 18:59:49 GMT  
		Size: 118.0 MB (117961188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57162c85dc433ca85c019d3fd46949e8e67dd9c9ed6d3eaf8e85b6c6bda9f631`  
		Last Modified: Wed, 21 Jan 2026 19:17:07 GMT  
		Size: 85.5 MB (85504468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1952b6374ea8f52566cb9d0a6254f913a68e889aa0156f06aa922380224b6ffe`  
		Last Modified: Wed, 21 Jan 2026 19:17:03 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cd80d0dc502793b77b5b24afa35952679e317020fea78d611415b6dd71ff6f`  
		Last Modified: Wed, 21 Jan 2026 23:58:53 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1d284a0bfc5fe39d4f3737fa9b0e0e7470bff481f54b13438dbbca2d66efa3`  
		Last Modified: Wed, 21 Jan 2026 19:17:57 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:4511fc969e83767269332d0413715b734f30e6d5c865dcd63f585b2d1bebf284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11649057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffd8f5b73adc0c5927d57f5181b25cc43c887e764f0b97ff33fdf754d37f415`

```dockerfile
```

-	Layers:
	-	`sha256:f4599cbe2819ffc77898ae84e89af4b13cbafe22db2de2c266cda2d3ecdf949b`  
		Last Modified: Wed, 21 Jan 2026 19:17:58 GMT  
		Size: 11.6 MB (11628020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5b07f8ce2b2cfe621182eacf4408a84d3cdfd40377384384397f0f167a4225d`  
		Last Modified: Wed, 21 Jan 2026 19:17:57 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
