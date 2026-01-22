## `gradle:jdk25-corretto`

```console
$ docker pull gradle@sha256:0a6f7a766a105fb04fe12d532af9540af5f32e4f98eff8e89a3e60757865be87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:650ff2d9450ab9aa4d5d363c395a91e25aae08ac7d38d7f887b6c74371fb236b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.3 MB (466265264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd18f6017e97786ad9cbb22e2c5dbc4aab1f431f213dea29a8d6fac435de0534`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:01:49 GMT
ARG version=25.0.2.10-1
# Wed, 21 Jan 2026 19:01:49 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:01:49 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:01:49 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 21 Jan 2026 19:11:01 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:11:01 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:11:01 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:11:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:11:02 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:11:02 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:11:02 GMT
ENV GRADLE_VERSION=9.3.0
# Wed, 21 Jan 2026 19:11:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Wed, 21 Jan 2026 19:11:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:11:04 GMT
USER gradle
# Wed, 21 Jan 2026 19:11:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 21 Jan 2026 19:11:04 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84184861cf3f73b067f6e2b91043dbc78ff544f7b571af6af75864a9e885dba`  
		Last Modified: Wed, 21 Jan 2026 19:19:38 GMT  
		Size: 189.2 MB (189191314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389cd3a79911c42cd9425b2215fdcb089b6d1f2c1e378be8f3e7debb43b8e085`  
		Last Modified: Wed, 21 Jan 2026 19:11:33 GMT  
		Size: 86.0 MB (86036601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db92992fab8e92e1022a95244dde113ab449908cbff682a3ae47ffef512026da`  
		Last Modified: Wed, 21 Jan 2026 19:12:03 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21f9ce5822c9b6db3f4ff1f3cc145e896db2676ffb688577a86957ea28e6669`  
		Last Modified: Wed, 21 Jan 2026 21:27:23 GMT  
		Size: 137.0 MB (136988868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794de2cf10b9a51412359f0ff4db33c6833b876db2a4e717ae6eeb31b89786e9`  
		Last Modified: Wed, 21 Jan 2026 21:27:25 GMT  
		Size: 25.6 KB (25594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b368f5141ca3990e9da6e6b66cbc901e123e9947955a60b891f0ffae86ff72a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11360579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ebd69cc37410319b5134fc7c9997ea933331a1725154e0e4a4b8d11abcf89f`

```dockerfile
```

-	Layers:
	-	`sha256:0eaacb2496e4cb32ee157b32eaeeb0b8a170a1b36b9aa268c50f554d02ba46a0`  
		Last Modified: Wed, 21 Jan 2026 21:24:17 GMT  
		Size: 11.3 MB (11338311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccb60ce3e124fcc3a58c974232ff441e2cd74c663fea8fb4c8d6d4938fda87c`  
		Last Modified: Wed, 21 Jan 2026 21:24:18 GMT  
		Size: 22.3 KB (22268 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d581e6dea7cbcfec3636cd21116c89532f439571952be5bae5b418a518d77269
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.5 MB (462541953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0caa8bd31ee0943f8cfa426e2452a501bf457005eba4fccf4a2e5856a4094d13`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:02:03 GMT
ARG version=25.0.2.10-1
# Wed, 21 Jan 2026 19:02:03 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:02:03 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:02:03 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:02:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 21 Jan 2026 19:11:27 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:11:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:11:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:11:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:11:27 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:11:27 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:11:27 GMT
ENV GRADLE_VERSION=9.3.0
# Wed, 21 Jan 2026 19:11:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Wed, 21 Jan 2026 19:11:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:11:30 GMT
USER gradle
# Wed, 21 Jan 2026 19:11:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 21 Jan 2026 19:11:31 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1219b2dc527a7d7920fc18d43a9d921a6ec165aad6ec37677541ec00415a03`  
		Last Modified: Wed, 21 Jan 2026 19:11:01 GMT  
		Size: 187.1 MB (187090489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9154e93f67f91c12d9281c172f757a052d1338bf9ec0b4305512786b865cb36`  
		Last Modified: Wed, 21 Jan 2026 19:12:02 GMT  
		Size: 85.5 MB (85517236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a892878d0dd3438890fec7ddd124d76d175c717c8e8c2f0db1bf352e8d351e4`  
		Last Modified: Wed, 21 Jan 2026 19:11:59 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7003ce126e0194d795feefe73f312a1ac0b3735453b449c09420c49873e6e4fd`  
		Last Modified: Wed, 21 Jan 2026 21:28:14 GMT  
		Size: 137.0 MB (136988868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1de6c8231323d3ff54072dde0396d72e60928fc1d4ded4a199dd233b5a0f925`  
		Last Modified: Wed, 21 Jan 2026 19:11:59 GMT  
		Size: 29.3 KB (29322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:6742c78d6e39f1e26751ce0f1ad3a460422b41d3870c6fa7a28ae8dc9ac02022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb559d3453413c88dc36174b0ca8055337b4ff91ac06d465d0da793a7cfc693`

```dockerfile
```

-	Layers:
	-	`sha256:c9ecde45f5634f9bfa9a9d678c21141f6904b5b19a5fcb54ddb414c1db69ffd8`  
		Last Modified: Wed, 21 Jan 2026 21:24:27 GMT  
		Size: 11.3 MB (11337348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2617598fff2916f7296460130a719904a4ad9829fdb6eb7825c7318549b410c0`  
		Last Modified: Wed, 21 Jan 2026 19:11:59 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
