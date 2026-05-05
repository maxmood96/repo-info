## `gradle:jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:d05a07d4ef85ceea122e227772e0503863fae2967021469832fcfa54c763f186
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:0e0eacddf520a37763d396c587ed15a9f1bb9862b42c3151b78a394b49742e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451451969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cc9f01e183154d8382923ac11b9a7dda283e0c949c5c360310f89a7af6b391`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:50 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:12:50 GMT
ARG package_version=1
# Mon, 04 May 2026 20:12:50 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:12:50 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 04 May 2026 20:41:43 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:41:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:41:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:41:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:41:43 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:41:44 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:41:44 GMT
ENV GRADLE_VERSION=9.5.0
# Mon, 04 May 2026 20:41:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Mon, 04 May 2026 20:41:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:41:46 GMT
USER gradle
# Mon, 04 May 2026 20:41:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 04 May 2026 20:41:47 GMT
USER root
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab4abe70d3e0dd1691b652885ef0ec24e3f6f3309fef057e815fc11525aff9c`  
		Last Modified: Mon, 04 May 2026 20:13:13 GMT  
		Size: 170.4 MB (170444396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac57e394e361dba895e843f558d61429519f36d76480f63da2bcb063d7723d28`  
		Last Modified: Mon, 04 May 2026 20:42:18 GMT  
		Size: 86.2 MB (86167578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be073c9e2d1f36d414ac3e93a19033c009eba5caab4b366149cdc586749bb90`  
		Last Modified: Mon, 04 May 2026 20:42:14 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4da7c9df480074e22d6bebd95fddf59ace5022ed7c86fab997db09503ec9082`  
		Last Modified: Mon, 04 May 2026 20:42:19 GMT  
		Size: 140.2 MB (140235935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c1f72f16b45d9565c3df2dc915b328508994c457b43d521e03edf917c7cd0f`  
		Last Modified: Mon, 04 May 2026 20:42:14 GMT  
		Size: 25.6 KB (25626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:8c73a33c3f71563244aaa26d0dc609555a381d96fdcb46ad6a3460b77ce70b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11389737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85911abdfe9276793f9e238180a726c2b0b135ebece98bfc78d5899a0a4ad136`

```dockerfile
```

-	Layers:
	-	`sha256:efef9f8b8e9877cc63483a98181107d2a0722ede9f0bef99304b2946c72d5354`  
		Last Modified: Mon, 04 May 2026 20:42:15 GMT  
		Size: 11.4 MB (11368086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cca67796782e4553b12da0a0dac4de261b9f5efb5e35fe0f3f32e80c70154231`  
		Last Modified: Mon, 04 May 2026 20:42:14 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:33ac3450f959a2b62eb6fedf16c36a7b7031ffdf150f3072b9678ab5d081c604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.1 MB (448102606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70febfaef5d26d08b842316f84ecbc35713276557e37a659042912ff00efcd5b`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:26 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:12:26 GMT
ARG package_version=1
# Mon, 04 May 2026 20:12:26 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:12:26 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 04 May 2026 20:41:43 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:41:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:41:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:41:43 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:41:43 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:41:43 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:41:43 GMT
ENV GRADLE_VERSION=9.5.0
# Mon, 04 May 2026 20:41:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Mon, 04 May 2026 20:41:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:41:46 GMT
USER gradle
# Mon, 04 May 2026 20:41:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 04 May 2026 20:41:46 GMT
USER root
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fe57dcd920a0d80a8ee81f1f0da4f9113f4389582ae792de57ec8d1defcda8`  
		Last Modified: Mon, 04 May 2026 20:12:52 GMT  
		Size: 168.7 MB (168722227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd0f3fe8d8549a60bf6476b8acfa37309a7c7ea69efc58eb334f908125d4585`  
		Last Modified: Mon, 04 May 2026 20:42:18 GMT  
		Size: 85.7 MB (85656661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e76a04bdf4461a24959c7be3267c2a1f3c6851ee05bf928225c0466acd77f90`  
		Last Modified: Mon, 04 May 2026 20:42:15 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ecf5f44d2b5711517ac74ba16dd80dc1a8a3099f6fd1aef9c5fa2a951a371a`  
		Last Modified: Mon, 04 May 2026 20:42:20 GMT  
		Size: 140.2 MB (140235935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f782e71e3cbb40ef2bdcc89007e3dd5b6ef70e9ac457d24dfec60f98b822e4`  
		Last Modified: Mon, 04 May 2026 20:42:15 GMT  
		Size: 29.3 KB (29333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:290ad3606138bc9934acbf6ad21c9cbb7aeb935061395d0f0aa3650499af8d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11388937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb478f7cc69071ad555c7638bbcb010db989af6e1ab586c11e7c0b88285689a`

```dockerfile
```

-	Layers:
	-	`sha256:25ade542f996b9bc1f687d630e4dd24d162371c0662d5731be9c1686778fd3f7`  
		Last Modified: Mon, 04 May 2026 20:42:15 GMT  
		Size: 11.4 MB (11367089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f85a0623ccb5aad0875463990489f96c0f4f03c4542b5311c63834f8fece77d`  
		Last Modified: Mon, 04 May 2026 20:42:15 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
