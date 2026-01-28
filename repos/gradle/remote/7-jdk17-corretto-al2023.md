## `gradle:7-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:8db3f4a0a4379d0c0b5cb2e8110301f7c461b53d2ad694e205d447afc888443d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:8587de38f516a040b8a3d1468a41f730c023bbd78e863d3a1750ec2e5662f877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.5 MB (425499581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe24a6d72a63636ad359030e86eb80560f3a8793da3c0ee25e4bccc3f03940b3`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:08:04 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:08:04 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:08:04 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:08:04 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:08:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 28 Jan 2026 04:56:10 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 04:56:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 04:56:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 04:56:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 04:56:11 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 04:56:11 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 04:56:11 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 28 Jan 2026 04:56:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 28 Jan 2026 04:56:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 04:56:14 GMT
USER gradle
# Wed, 28 Jan 2026 04:56:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 04:56:14 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f764ca21eff5f12dc46762e7c29c7efe1ac48c3ad2653b8f68ac3c495c0b82`  
		Last Modified: Wed, 28 Jan 2026 04:08:26 GMT  
		Size: 156.9 MB (156915347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fdb5c4676242290dbc7197226aa2beb9e5fb86db3d89c64a4cda9cd2279b21`  
		Last Modified: Wed, 28 Jan 2026 04:56:44 GMT  
		Size: 86.0 MB (86034400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b3b394559a74c1e60f744a77373ce681e42f131cfacb2b1d5ddbdf37da341`  
		Last Modified: Wed, 28 Jan 2026 04:56:41 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b95247fc8525aea5a8fc0a591421b436afe902a8ae5fef9419bc1f4a5c76b6`  
		Last Modified: Wed, 28 Jan 2026 04:56:45 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c025da00273f8c3311f9053d5b284cf1954d3635dbe09808d3e4c48a4486c42a`  
		Last Modified: Wed, 28 Jan 2026 04:56:41 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:3d92e0347b6d196aad11d1387b6cce14eeae77a5d19d57c9955aa85e08bb7020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11271182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b410ca6e5032a6f662d68afb335823637753f0487b39e01a4db02a6c0ab408`

```dockerfile
```

-	Layers:
	-	`sha256:c3870cf013de63460903f634b07ed168b2cd4f4586d3accec8dcc9ab9cf5f0e3`  
		Last Modified: Wed, 28 Jan 2026 04:56:41 GMT  
		Size: 11.3 MB (11250469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d2ffcec15c639e3f15438047644d23bee8f21e4905f0f00bf98d3656f3a7f4b`  
		Last Modified: Wed, 28 Jan 2026 04:56:41 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:2c66107d5a0fa3a12f539a7b7de1d741e0fab77b2bc8aa236252f46fe23981f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422684085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bcbb72e979ff6f36c91f22e7e5939ce1d7b3fb8d8d84c786a454f61c580542b`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:28:33 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:28:33 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:28:33 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:28:33 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:28:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 28 Jan 2026 05:38:14 GMT
CMD ["gradle"]
# Wed, 28 Jan 2026 05:38:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 28 Jan 2026 05:38:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 28 Jan 2026 05:38:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 28 Jan 2026 05:38:15 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 28 Jan 2026 05:38:15 GMT
WORKDIR /home/gradle
# Wed, 28 Jan 2026 05:38:15 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 28 Jan 2026 05:38:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 28 Jan 2026 05:38:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 28 Jan 2026 05:38:17 GMT
USER gradle
# Wed, 28 Jan 2026 05:38:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 28 Jan 2026 05:38:18 GMT
USER root
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0aad64ff72b39223fe7c89c4c32e0df701234a6d10e6450afd2c590b69880b`  
		Last Modified: Wed, 28 Jan 2026 04:28:55 GMT  
		Size: 155.7 MB (155720069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1683f81a7f274bb0e296021fd1e2e355fa36001f484f809f976f019e160e17ea`  
		Last Modified: Wed, 28 Jan 2026 05:38:49 GMT  
		Size: 85.5 MB (85516758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8032c09d748585585113da6ed642f51d534fedfb3cad3b8d468fcb67e7c5f5d0`  
		Last Modified: Wed, 28 Jan 2026 05:38:46 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afbdcb4a1282c42637eef98d486704d393c9342402aca47e7f2e7ae33f332ef`  
		Last Modified: Wed, 28 Jan 2026 05:38:50 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba85a9e63afbe6e633874c5dfd99ed182448cab99608f708621828ad4fd1076a`  
		Last Modified: Wed, 28 Jan 2026 05:38:45 GMT  
		Size: 59.5 KB (59523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:6c74bcd4ab481d412c55caf75cc0b11e2669cb139d77c8173dbbe6c2bee313bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11270330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9b656d976f7f3a7d780a7c5add38765f3fbe9d31aaf143431d44ad3a418f57`

```dockerfile
```

-	Layers:
	-	`sha256:f3f7561a9ae68aba23f8fe4d934fba6543efc7c44a14670d5448f654ba7e01fd`  
		Last Modified: Wed, 28 Jan 2026 05:38:46 GMT  
		Size: 11.2 MB (11249444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4aebe828d54fb010effb6142a0f9b9f1187c33be16c9182227af747187776b`  
		Last Modified: Wed, 28 Jan 2026 05:38:45 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
