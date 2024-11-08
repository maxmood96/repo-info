## `gradle:jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:1484b9f905fdb9705c5d23b3d8235ab5fdc96b205fef2b42d6cc3f0aac737ac8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:96ef5fcb22f37d4bdbe23ec562036fc9bf52c48ca85492f28bbdd03f9539689b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **527.5 MB (527511442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df5939353dccaed7e6903468a9b70e344d017da33ff1777491b241d3680cc6c`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 06 Nov 2024 04:13:47 GMT
CMD ["gradle"]
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Nov 2024 04:13:47 GMT
WORKDIR /home/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 06 Nov 2024 04:13:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER gradle
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER root
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fba7f20e688d8386a7abf38f9c39f6b1cf3d2a2489ec2414421b89bf44b1c19`  
		Last Modified: Mon, 21 Oct 2024 18:57:57 GMT  
		Size: 288.8 MB (288796695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4694c7cf9a3433dd30bb246e097fe74f573f42c81e8eabd3d3b5f7f4238c5f6b`  
		Last Modified: Wed, 06 Nov 2024 20:18:33 GMT  
		Size: 49.6 MB (49584593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f0853d41d83d70787f845f5785056c0cfc49b945461de81213d1e46adae5b1`  
		Last Modified: Wed, 06 Nov 2024 20:18:31 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6f479962d362b7e25d7cf871eb95d601dca6396282a91af741658e73172701`  
		Last Modified: Wed, 06 Nov 2024 20:18:35 GMT  
		Size: 136.7 MB (136729736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f375ba376013ddda3b62c779de56cbe8750fa8a0f6d87e48694d88791b0217e`  
		Last Modified: Wed, 06 Nov 2024 20:18:31 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a903bfd6d606a746b1cb26c216029f868dd3ea8c02571fa93d1abd1bba15d5ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.5 MB (16489533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724dd41224621ba26708bc661a69125a396d59d373ac9645bd04171179ba6770`

```dockerfile
```

-	Layers:
	-	`sha256:97a4be61df4b41d9b7c098ce75bc28350df9b12af01315b93a0bfe9cec07cef9`  
		Last Modified: Wed, 06 Nov 2024 20:18:32 GMT  
		Size: 16.5 MB (16469635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23108c06114691a48dc90a5f3f5d320ab1c19a0e93393374f6a47ea5b7b5325`  
		Last Modified: Wed, 06 Nov 2024 20:18:31 GMT  
		Size: 19.9 KB (19898 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e05702b047489ee96326470f121e61d9a10c78f8f380e2316ed33018172e83af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.2 MB (377168042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1843e0ab3a7381233a59d2009ffab3abe94d38baa18c717eeb7a255c5cae8e65`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 06 Nov 2024 04:13:47 GMT
CMD ["gradle"]
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Nov 2024 04:13:47 GMT
WORKDIR /home/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 06 Nov 2024 04:13:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER gradle
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER root
```

-	Layers:
	-	`sha256:ec188ec9ab67d19829a9f75d24a165b6b31e1c611a03fdfabfdf4f1950a2c30a`  
		Last Modified: Wed, 06 Nov 2024 22:31:41 GMT  
		Size: 51.4 MB (51424001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f0f3bbcccef20d95e228e1d90d7760464c9ef63c0052d7126ff526ca9f600a`  
		Last Modified: Thu, 07 Nov 2024 21:48:21 GMT  
		Size: 118.6 MB (118618199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c3d76634b2ef3476b4cb2024bf34a9e9d62d361fdef74f9e121604b0b212c7`  
		Last Modified: Thu, 07 Nov 2024 22:48:36 GMT  
		Size: 70.3 MB (70334899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd8376bc98cb7c45550f0714b3012571c7b9d572003365a6871b12ef6ef44b2`  
		Last Modified: Thu, 07 Nov 2024 22:48:33 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca1ff9ed900b54f2256131b7536ec766062a8e1b2c29bc801dd8b0ed2c8497`  
		Last Modified: Thu, 07 Nov 2024 22:48:37 GMT  
		Size: 136.7 MB (136729734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb3743cbc8b14b371a5a875277fccb6127259190665ddd446b3d5d7e6d2973d`  
		Last Modified: Thu, 07 Nov 2024 22:48:34 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:3fa4803ca07f373f1a8298e9dc14fe3bc7b1dc7f89314261d97a02ca7a3ce416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11128518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6470a37a10c4a5dd891e70f2b36f7db1851068909fdc71003d06cc100ef92e`

```dockerfile
```

-	Layers:
	-	`sha256:d4020982678d3cc30839508e68ceec2968c3a8bba2cdfe80fd5d2a1d969a01b2`  
		Last Modified: Thu, 07 Nov 2024 22:48:34 GMT  
		Size: 11.1 MB (11108424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d93868f28b29b603d0eedd5e3c1eaa53c581f0ea219fc83175769e754f5d38ba`  
		Last Modified: Thu, 07 Nov 2024 22:48:33 GMT  
		Size: 20.1 KB (20094 bytes)  
		MIME: application/vnd.in-toto+json
