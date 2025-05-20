## `gradle:8-jdk8-corretto`

```console
$ docker pull gradle@sha256:1a20beaf0fe1737038fe43f4f0ad94e43400910ee68d115a9810b3e6d5617029
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:78cb7655a863f701119bcd60f5e4e053bfe4502296e3a3ae1ab95f011cdf71b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **573.5 MB (573548233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f53d4d5e916c3589a1d93d985cea75600317f4410b3a45dc79b0a595b7be55`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 26 Apr 2025 01:26:29 GMT
COPY /rootfs/ / # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
ARG version=1.8.0_452.b09-2
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV LANG=C.UTF-8
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Wed, 14 May 2025 01:42:44 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fe6cf55dc3adf66743afc67d7bcfc0ce974e2646080ac95d6c204123e58662`  
		Last Modified: Mon, 19 May 2025 23:37:53 GMT  
		Size: 330.7 MB (330665928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6308473be14ae84aaac92e3187e721d51c1cd190659b0776643805a5b2aa3b76`  
		Last Modified: Mon, 19 May 2025 23:47:09 GMT  
		Size: 51.8 MB (51816178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bacb895404bcb8b69a7b3f2bbfdbf6c2f52d254a9bfd3dc257be365ec9bc399`  
		Last Modified: Mon, 19 May 2025 23:47:08 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76ced12f6e8c9feb7b9ca5aff5754c31b865bbd7c349b729d9c0f8757185d17`  
		Last Modified: Mon, 19 May 2025 23:47:10 GMT  
		Size: 137.4 MB (137394549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f177282f0a53b18fa7fe0c6e58f932fc95fdf020812b7eaabc1c53c3a3e5f6f`  
		Last Modified: Mon, 19 May 2025 23:47:08 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:86a9c763d43d361179b99ffaa6e25b36c1a18189fc19e1b39d6e6b602b0dc0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17628907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e482b17c6f410634debe6619082da455a366efe7dc9eff507b2088aae12a45cb`

```dockerfile
```

-	Layers:
	-	`sha256:756cbb404cf9750c0fb4f9d63bf742b03467943b1a451dbf29928c72a9c083be`  
		Last Modified: Mon, 19 May 2025 23:47:08 GMT  
		Size: 17.6 MB (17609013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be2b867f6fc467003d9514699f465c28b06033c280cd17bf029070eaff59fc28`  
		Last Modified: Mon, 19 May 2025 23:47:08 GMT  
		Size: 19.9 KB (19894 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:897f856ea8a80d9a6fb095637f12340adf4d0f3044552067d02cd396b15ba681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.9 MB (379881811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c955a0f3f7566bc17c9bd4aa999247f5d453dc3d6eedc298051a4ce0f4ea06`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 26 Apr 2025 01:26:29 GMT
COPY /rootfs/ / # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["/bin/bash"]
# Sat, 26 Apr 2025 01:26:29 GMT
ARG version=1.8.0_452.b09-2
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: version=1.8.0_452.b09-2
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
ENV LANG=C.UTF-8
# Sat, 26 Apr 2025 01:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Sat, 26 Apr 2025 01:26:29 GMT
CMD ["gradle"]
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 26 Apr 2025 01:26:29 GMT
WORKDIR /home/gradle
# Sat, 26 Apr 2025 01:26:29 GMT
ENV GRADLE_VERSION=8.14
# Sat, 26 Apr 2025 01:26:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER gradle
# Sat, 26 Apr 2025 01:26:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=61ad310d3c7d3e5da131b76bbf22b5a4c0786e9d892dae8c1658d4b484de3caa
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 26 Apr 2025 01:26:29 GMT
USER root
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Wed, 14 May 2025 01:42:43 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ba910b575edfd05c7f13065f2a17cff35d62e2af5009fcfda96edd05eb5b25`  
		Last Modified: Mon, 19 May 2025 23:47:42 GMT  
		Size: 117.8 MB (117849549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5d3f3c342c5a61fea1be9d7e82a6e0a800aae741d73c389ed6f498f6195e74`  
		Last Modified: Tue, 20 May 2025 00:30:33 GMT  
		Size: 72.0 MB (72010762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a965c5ccfa78310147421e6af0ce77c47c28484b26c7fa3e2859304535ddcdc5`  
		Last Modified: Tue, 20 May 2025 00:30:31 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a40b965224924bf61e17ff3f7986474e4311e1f8c9c7bb11921e668cf4ff99`  
		Last Modified: Tue, 20 May 2025 00:30:35 GMT  
		Size: 137.4 MB (137394548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ac2d01134411d804b7fa2be2ab01c71a012f1f9f083ca6b779b82830c92e1d`  
		Last Modified: Tue, 20 May 2025 00:30:32 GMT  
		Size: 59.5 KB (59533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:73d46cc3c1567af1c7ffb0a6dfd28cbe2cb8329f62082a5f2aa44d550e4c2467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11193942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27f81c38c427ef948d43dcdc26db5d30e8553e6b38b015692e1dc29c50fdf9e`

```dockerfile
```

-	Layers:
	-	`sha256:029902e44e18218d25c27c93dd1f365a6d85f5f2793d4f13864247660d2ba5de`  
		Last Modified: Tue, 20 May 2025 00:30:32 GMT  
		Size: 11.2 MB (11173851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f0655318230c1dcc2e431f80eda1b027477127fd2efd23fbb896b137a07a684`  
		Last Modified: Tue, 20 May 2025 00:30:31 GMT  
		Size: 20.1 KB (20091 bytes)  
		MIME: application/vnd.in-toto+json
