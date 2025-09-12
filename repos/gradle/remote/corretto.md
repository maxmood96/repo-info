## `gradle:corretto`

```console
$ docker pull gradle@sha256:fdaa47a981d517e35e61d606d6e86955ffc6b227305603349104697b3df8676a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:corretto` - linux; amd64

```console
$ docker pull gradle@sha256:ab0b2c45d7eeceefb3967a87311f761cbce24af339bbb7bf36c21b21a2b1ef6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.1 MB (444072514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1dd497a2bf1c7923646b09993e72ca64c3a0894bf479d14e114b55ae3b2a03`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER root
```

-	Layers:
	-	`sha256:0727f841555e830a24054117b5d53ecc18438e2e82fc78dd3cc766ca6bb76cab`  
		Last Modified: Wed, 10 Sep 2025 02:33:49 GMT  
		Size: 53.9 MB (53875706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b277a99eedd058e5435ee84d1bf1db6bfc8c7b5b9a602de4fe6a22df9fc96cb`  
		Last Modified: Fri, 12 Sep 2025 02:10:37 GMT  
		Size: 170.1 MB (170108136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc9315f93cfe1982427dceeebddaa411a62505594d476670feeca649770520b`  
		Last Modified: Fri, 12 Sep 2025 02:12:03 GMT  
		Size: 85.6 MB (85551253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fe98fe8320bf4acf8eaad52c99363b43f61ea39076ad8c7b9f960ab2dde8f9`  
		Last Modified: Fri, 12 Sep 2025 02:11:58 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c9f48ab3ef2dc4a969685f3be5b563abdcf50731680430311db5d37dfdf1f8`  
		Last Modified: Fri, 12 Sep 2025 05:28:00 GMT  
		Size: 134.5 MB (134480832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14c482157a7cbcb977dbb09fea95fd78c5e97e8c5df6cf0eca5940b92cbe051`  
		Last Modified: Fri, 12 Sep 2025 02:11:58 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:68e8b73336deb09aa4b6a3e506f054ab6a4109952b02255ccb1ea9a812918261
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11323524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a41db8a4534a78fb92ec6f8a8691d4ab37f8ca68af2d3253f6f684f72cdefc`

```dockerfile
```

-	Layers:
	-	`sha256:aea5949fe5c5730724055e60aff994a84ec329a0a096e9e9cee240a1c6e86093`  
		Last Modified: Fri, 12 Sep 2025 05:24:50 GMT  
		Size: 11.3 MB (11301350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b37e205909f0a517b953191727363b0ac5b8fce6411d209672d3e8dda6390866`  
		Last Modified: Fri, 12 Sep 2025 05:24:51 GMT  
		Size: 22.2 KB (22174 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bf53c5e1edc85cbbf9f6ae785bf98b021c9ae75362062bad10a3546a0cc30a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.8 MB (440794815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e5b67727d0e18f1196a4befefa5a977f34bbcb68b84afc6ceabdcbfce26d99`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER gradle
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
USER root
```

-	Layers:
	-	`sha256:a2133584a03a0323a461f4ba1900a168268d3305d6206a4e0a210c92b146e94a`  
		Last Modified: Wed, 10 Sep 2025 02:34:05 GMT  
		Size: 52.8 MB (52775111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d786316b8ae5b77f46f5dc354d692fb53f0aa9de45255ab4023dae3113e84466`  
		Last Modified: Fri, 12 Sep 2025 02:11:09 GMT  
		Size: 168.4 MB (168399303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16890bbce5c26a976c853b773bf13d23b94526baccec73d7dc86c81e5b251709`  
		Last Modified: Fri, 12 Sep 2025 02:12:36 GMT  
		Size: 85.1 MB (85078362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109bd291f2769a306ae10e1273df51a516b1d3518ade86698fdbf6c39764ab59`  
		Last Modified: Fri, 12 Sep 2025 02:12:31 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b87801483a906cf3f341b4f4fb3381a9b79f06c05e4d757fa7bb517985ae93`  
		Last Modified: Fri, 12 Sep 2025 05:44:47 GMT  
		Size: 134.5 MB (134480832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dd2effd1b292a2f49d07e48e3f37b552125f6b993e0908ab8fdf752c7ba29a`  
		Last Modified: Fri, 12 Sep 2025 02:12:31 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:4950f00442c1a85544be9855ed6a0b11f0c5f54db01de219b847514749ef14e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11322771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40dd87d41d4a6c3fbcd06401d244da5fdde6a55ec6c7fe60c59ffd945d29cf1`

```dockerfile
```

-	Layers:
	-	`sha256:d3297b0e35ccd22556ea945d7fc4cd40bcaa92be79de175987b4e4565409d100`  
		Last Modified: Fri, 12 Sep 2025 05:25:00 GMT  
		Size: 11.3 MB (11300376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0fbe9957ac76475e0bf871982fd534d38c682588be34eb81ac4e7e145dcb0a`  
		Last Modified: Fri, 12 Sep 2025 05:25:01 GMT  
		Size: 22.4 KB (22395 bytes)  
		MIME: application/vnd.in-toto+json
