## `gradle:9-jdk17-corretto`

```console
$ docker pull gradle@sha256:66ddd8cb741714c8d931040fcc88d8e05fba5732a9537b7d980cd589c1ab1f7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:15f4a86905227edef08985b5c28f410cd5c482014098bec9fcc25113b6b4a1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.0 MB (438995098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdddeff2570b419ead207ef0ebb89c500f8857c2bf8b22e02a7cec07d4e47c4`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:06 GMT
ARG version=17.0.19.10-1
# Mon, 22 Jun 2026 18:05:06 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:06 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:06 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 22 Jun 2026 18:15:13 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:15:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:15:13 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:15:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:15:13 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:15:13 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:15:13 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:15:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:15:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:15:16 GMT
USER gradle
# Mon, 22 Jun 2026 18:15:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:15:16 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123c983efb3d9caab78dd5f7e804d4131aca7970c4f8c80cdc377a8fc76a1809`  
		Last Modified: Mon, 22 Jun 2026 18:05:28 GMT  
		Size: 157.2 MB (157157640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d811a000c148c2cf9c462672c4c306367e3e2f9a585c08db351dd3c2296ff12a`  
		Last Modified: Mon, 22 Jun 2026 18:15:49 GMT  
		Size: 86.6 MB (86640887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fdd2ff8d9bf9401da1d69cf46d949047f322b406134b20f8cd12f92c2a23a7`  
		Last Modified: Mon, 22 Jun 2026 18:15:44 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13869eaebdc9650d9c67d41a9fbcdc20ce81d78eed887ce53f039af243ab68eb`  
		Last Modified: Mon, 22 Jun 2026 18:15:49 GMT  
		Size: 140.6 MB (140595106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cb27bf94490c7a77555e0b63eb3f8de6003f2d2eba61e06d2fb377e2d2b9e5`  
		Last Modified: Mon, 22 Jun 2026 18:15:44 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:f0aef4d57cc3c1b177f7e7b7dd672fbf233080825d2e9903e5295838d1493f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11404130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db4d9ee77dc2cf0358547ec1d942a1d3001a5c23ecc4cea264aabed315101ba`

```dockerfile
```

-	Layers:
	-	`sha256:ce7e26ccd05832a206770a7c761e7edfd15e7d79599cdf6f85d50fc8f38dc158`  
		Last Modified: Mon, 22 Jun 2026 18:15:45 GMT  
		Size: 11.4 MB (11382633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:493874a89383daca7036b7df772df6fc6b27b2cd4c7972c42971da8b80a30ebc`  
		Last Modified: Mon, 22 Jun 2026 18:15:44 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ac1e1d14d5f5ffd18a633e26fcd5bb2ad7fd9515f29592040ce986295fbcc303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.1 MB (436099504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa9174728c8df1225362e0974fa61c74d8c6ca2e30aac132a9ed48132273cb7`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:43 GMT
ARG version=17.0.19.10-1
# Mon, 22 Jun 2026 18:14:43 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:14:43 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:14:43 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 22 Jun 2026 18:25:40 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:25:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:25:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:25:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:25:40 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:25:40 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:25:40 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:25:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:25:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:25:43 GMT
USER gradle
# Mon, 22 Jun 2026 18:25:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:25:44 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e6827a1bd934536bbaca8ee73b82a907a6f504f2a8c7bf2da0903d11d72d4b`  
		Last Modified: Mon, 22 Jun 2026 18:15:06 GMT  
		Size: 156.0 MB (155988813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500630aaa3f7dcc4766e064a957000a66ed958e38362bcec5dbeae6d090ecb2f`  
		Last Modified: Mon, 22 Jun 2026 18:26:15 GMT  
		Size: 86.0 MB (86033888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c302c011cb96405db4a262e6a13d51087c2a9a8714308acb03b5cda100df2c`  
		Last Modified: Mon, 22 Jun 2026 18:26:11 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aba1180051819f9baedbb7a080b8ba29a7a99efa832f5fe75ded1af81615c3`  
		Last Modified: Mon, 22 Jun 2026 18:26:17 GMT  
		Size: 140.6 MB (140595106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f1972d7dec0eacd3dbdbc8a992e226cb5368e2c58edca3af52b2e1742f885b`  
		Last Modified: Mon, 22 Jun 2026 18:26:11 GMT  
		Size: 29.3 KB (29332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:aac2044842770e5d47441711fc36be43118bc2b8fbefa080d8df7f2c609c2d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11403327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7402d1416870beebf5d4bd01600464b41c3f7d7487263221368be9c6f51cb209`

```dockerfile
```

-	Layers:
	-	`sha256:46e9fbedcaf85691c5e47a46642cf07771c1109661da490034bf9d8345047982`  
		Last Modified: Mon, 22 Jun 2026 18:26:12 GMT  
		Size: 11.4 MB (11381633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2104958e1fe3ff6a04858ddcf8b62a78555636bd8eb98bd61e99378b9112a8f1`  
		Last Modified: Mon, 22 Jun 2026 18:26:11 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
