## `gradle:jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:87431079ae8c0fa297c89e834f5a39b7c616bd656085bc074e537b380e6080e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:8286c5f4b77803c32931a03f05f60408d456d712762f65a0f52854a0b6559efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.1 MB (589117900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e25078598dfa0c8372653dcf2ea75ef2fb522177049b588bf378dc0454f71d7`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:11 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:11:11 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 09 Jun 2026 22:05:56 GMT
CMD ["gradle"]
# Tue, 09 Jun 2026 22:05:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 09 Jun 2026 22:05:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 09 Jun 2026 22:05:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 09 Jun 2026 22:05:56 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 09 Jun 2026 22:05:57 GMT
WORKDIR /home/gradle
# Tue, 09 Jun 2026 22:05:57 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 09 Jun 2026 22:05:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 09 Jun 2026 22:05:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 09 Jun 2026 22:05:59 GMT
USER gradle
# Tue, 09 Jun 2026 22:06:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 09 Jun 2026 22:06:00 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c2e3cf8908eccca20edf90d28e3fee070f14d8c192deedf6386f8c0d9b165a`  
		Last Modified: Tue, 09 Jun 2026 21:12:09 GMT  
		Size: 330.8 MB (330825369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac679f99fa6bf65e68d386b05ec26ca0b9c63921b539ccf9ff0e53c6b5ad0089`  
		Last Modified: Tue, 09 Jun 2026 22:06:42 GMT  
		Size: 65.6 MB (65595963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39510000a8abf3695242afcfbb4b89f573aed3dc01895176cb11e28de239bd84`  
		Last Modified: Tue, 09 Jun 2026 22:06:39 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dfa30f1976a0fb9409d4f4cacb26de13093dc0e48f43ffc0a575c7133a1365`  
		Last Modified: Tue, 09 Jun 2026 22:06:44 GMT  
		Size: 138.1 MB (138068535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ea9ff2ed38941390f62638c595792ba23a363fce603a9cb70c81597c217eee`  
		Last Modified: Tue, 09 Jun 2026 22:06:39 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:7343b14effde68290a3094330d673d9f29ec6c6b32c1bbdd54308115dc65fa34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18185198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54921240252f95deefa700a000f0cd2ef487a77acef56b7872ea5ed94c9c7ef4`

```dockerfile
```

-	Layers:
	-	`sha256:3e229850448248ba59717da1940d5d99a4ef859ac72685c71d1581762ec6422e`  
		Last Modified: Tue, 09 Jun 2026 22:06:40 GMT  
		Size: 18.2 MB (18163544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d2417f52e89c7c37943b8bf2e59aba4b6d4ba1a447058f16c2badac189fc30`  
		Last Modified: Tue, 09 Jun 2026 22:06:39 GMT  
		Size: 21.7 KB (21654 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5e6562c7e93881e0ea6611f0b13647db4f81182b7ee39135228e5cd5220a664a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.3 MB (395260501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb112145a224e9bdfdd34d1506ad5b56e90921760fb95ac056c5e3ef486895a`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:10:44 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:10:44 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:10:44 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:10:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 09 Jun 2026 22:06:46 GMT
CMD ["gradle"]
# Tue, 09 Jun 2026 22:06:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 09 Jun 2026 22:06:46 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 09 Jun 2026 22:06:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 09 Jun 2026 22:06:46 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 09 Jun 2026 22:06:46 GMT
WORKDIR /home/gradle
# Tue, 09 Jun 2026 22:06:46 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 09 Jun 2026 22:06:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 09 Jun 2026 22:06:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 09 Jun 2026 22:06:49 GMT
USER gradle
# Tue, 09 Jun 2026 22:06:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 09 Jun 2026 22:06:49 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac744debc1aeda7f8a15a7e95c01905f3886e894cc1989142c7256e5bc4cdaca`  
		Last Modified: Tue, 09 Jun 2026 21:11:04 GMT  
		Size: 118.0 MB (117955626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8aa49587c1453651cea9f708a503c67e4d79bd944b0d3af2ba05d5aa0e487c`  
		Last Modified: Tue, 09 Jun 2026 22:07:21 GMT  
		Size: 85.7 MB (85717303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f5b4dc54a9367b72fc0959c36c45f65bfd66cec0ae1853640dea6815dc49bd`  
		Last Modified: Tue, 09 Jun 2026 22:07:17 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b648ed0cd260d690cd452a673539391500a7ad3164d6d1238f12063e012140a9`  
		Last Modified: Tue, 09 Jun 2026 22:07:22 GMT  
		Size: 138.1 MB (138068535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e7bbf4d78644d3c604c85abbcfa4e444718f29d4d6e7c75c332f6ed4ebc292e`  
		Last Modified: Tue, 09 Jun 2026 22:07:17 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:4a6bc430a8204c026a4b0bf930cd61597475e3ea66beb3318df7451b51c983ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11749571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceeae6e704df0c288a95d487075415fd0f832422e5839ea03146e80ec4a1015b`

```dockerfile
```

-	Layers:
	-	`sha256:c204a7f876024e79cc25fd5cdafa42a44487e7e04ac7dab14307d0c80a1f53be`  
		Last Modified: Tue, 09 Jun 2026 22:07:18 GMT  
		Size: 11.7 MB (11727720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36de07a6bd96edf66d93cbd13e22c9ce622e2a7efe557fcdd51fdc8f6157b84e`  
		Last Modified: Tue, 09 Jun 2026 22:07:17 GMT  
		Size: 21.9 KB (21851 bytes)  
		MIME: application/vnd.in-toto+json
