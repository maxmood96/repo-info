## `gradle:8-jdk17-corretto`

```console
$ docker pull gradle@sha256:26454f9019d49c2b3fddabccd2903041866f9463cdc84127b766d7b50435f083
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:fdd3a53584e65a197c1abece5e52472fec9c7c409cab29a9d8a901dc14873936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.9 MB (433947798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4254646a8b299460bb90c48f0726fe033fad602376a9b154b0845aeeb41b7fe4`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Sep 2025 16:01:58 GMT
COPY /rootfs/ / # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:01:58 GMT
ARG version=17.0.17.10-1
# Mon, 29 Sep 2025 16:01:58 GMT
ARG package_version=1
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
ENV LANG=C.UTF-8
# Mon, 29 Sep 2025 16:01:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["gradle"]
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Sep 2025 16:01:58 GMT
WORKDIR /home/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_VERSION=8.14.3
# Mon, 29 Sep 2025 16:01:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER gradle
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER root
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c18700ed5b667d3e3ad2c64896284eb1ca36287f16a71ecfb7d35d0da454038`  
		Last Modified: Wed, 22 Oct 2025 00:50:39 GMT  
		Size: 156.9 MB (156935240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a289b60636b1756f6c2b7c261024c20bf1feb4ca6560937be6c15c10bfc31bba`  
		Last Modified: Wed, 22 Oct 2025 02:40:41 GMT  
		Size: 85.6 MB (85555650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f43d4ba317af0596e7bd3e82c0afbe6917683540d798a4fca408ad4718c842`  
		Last Modified: Wed, 22 Oct 2025 02:40:35 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff8cbdbb1d37a9c2f98327dc0bd48340b7b7b2e9696f866fa44c71f0f0963c`  
		Last Modified: Wed, 22 Oct 2025 08:13:30 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b822b54fdd4bbe30ee54e0dd10f542bc3a99959bdb4a500661d262b3b3b3648`  
		Last Modified: Wed, 22 Oct 2025 02:40:35 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e1da1b2401919c8c0945cdd331058eef7bb0a8eb68d80d464b2cf5f38e4b7b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11332277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16d72bf9a1045638362dbe97da90902adf0e3fea4c8977ede6dea017cdf129c`

```dockerfile
```

-	Layers:
	-	`sha256:2bfb338a801d2e656aa26686218813d28e37e7f26d07a4c258f854a04863a381`  
		Last Modified: Wed, 22 Oct 2025 05:20:33 GMT  
		Size: 11.3 MB (11311507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f047f429b0b00a59991bd34a1cf2140f258f3233585c8ac53a4e2c8e13696047`  
		Last Modified: Wed, 22 Oct 2025 05:20:33 GMT  
		Size: 20.8 KB (20770 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bbd039cd3fde924fcba6bca74652aa3401d7fb7f6c268aa78d866c4409c4f904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.2 MB (431179427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55493ae145d08b98064a57af25408b963b1539e6113be2b36396989ffa5c82e`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 29 Sep 2025 16:01:58 GMT
COPY /rootfs/ / # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["/bin/bash"]
# Mon, 29 Sep 2025 16:01:58 GMT
ARG version=17.0.17.10-1
# Mon, 29 Sep 2025 16:01:58 GMT
ARG package_version=1
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
ENV LANG=C.UTF-8
# Mon, 29 Sep 2025 16:01:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 29 Sep 2025 16:01:58 GMT
CMD ["gradle"]
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 29 Sep 2025 16:01:58 GMT
WORKDIR /home/gradle
# Mon, 29 Sep 2025 16:01:58 GMT
ENV GRADLE_VERSION=8.14.3
# Mon, 29 Sep 2025 16:01:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER gradle
# Mon, 29 Sep 2025 16:01:58 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 29 Sep 2025 16:01:58 GMT
USER root
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6803c97e6c0d717ec8eb0dfce3611037cd37d1539766448f9235c54a09a795`  
		Last Modified: Tue, 21 Oct 2025 22:11:31 GMT  
		Size: 155.7 MB (155747849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058223ba12ac99569be6ddd4463310c724f82033d6e9da461234e5fd47b70fc1`  
		Last Modified: Wed, 22 Oct 2025 03:30:32 GMT  
		Size: 85.1 MB (85083971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f97de295ad332d2aa775eb0a1aaa0003a3fd759b361f572172697955e4360fa`  
		Last Modified: Tue, 21 Oct 2025 22:58:19 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9255daaf9e3dd7cd22b42e92a1bac4229c02f32f8e74f6b9bb6e0d49e2f4fbd3`  
		Last Modified: Wed, 22 Oct 2025 03:30:44 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5650291775419dacdd1eea26693ea2c28ca5a6d9789ee88a2213a182a2125398`  
		Last Modified: Tue, 21 Oct 2025 22:58:19 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:58321e4edc091131cb43d87bcbd99e59e38cebea76dace80df7b3c20ec85c02e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11331425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445ac64dfa9b59ee749b4e1c4e8fc254f83f5982a36b64d567bdc7b85d0e76cd`

```dockerfile
```

-	Layers:
	-	`sha256:a6027f9eacda3a8b7cb72553c31929105a545f07db428769d49b641bec9b3221`  
		Last Modified: Tue, 21 Oct 2025 23:20:32 GMT  
		Size: 11.3 MB (11310482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff0e643bc09e8d04cb993f9d43ba8b1be4fa98ca74e47322041c913d0c23e87f`  
		Last Modified: Tue, 21 Oct 2025 23:20:32 GMT  
		Size: 20.9 KB (20943 bytes)  
		MIME: application/vnd.in-toto+json
