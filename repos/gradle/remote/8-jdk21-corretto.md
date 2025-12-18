## `gradle:8-jdk21-corretto`

```console
$ docker pull gradle@sha256:27f3cd2ec8cadde82dbd677c8b4c18e54594cea72aa1c7c5a415436167629552
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:f28c1655374800bba3365bcea8471eba02f7ab950fbc15d42ff08f9425b3719e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.6 MB (447646520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd68fded0ff12d0b6d773cb31b72369496ba374b1b7e29cc8caf7c7c11594c51`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:18:40 GMT
ARG version=21.0.9.11-1
# Thu, 18 Dec 2025 01:18:40 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:18:40 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:18:40 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:18:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 18 Dec 2025 02:18:56 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:18:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:18:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:18:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:18:57 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:18:57 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:18:57 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 18 Dec 2025 02:18:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 18 Dec 2025 02:18:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:18:59 GMT
USER gradle
# Thu, 18 Dec 2025 02:18:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Dec 2025 02:18:59 GMT
USER root
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6113d4b7ab7a5acb2f4b4897a2154fedabeed4d6662b5afd47f2928b0778326c`  
		Last Modified: Thu, 18 Dec 2025 01:19:27 GMT  
		Size: 170.2 MB (170185789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f8ddc83f24b99fac07d362aa075bc9096c20221ec223bc4e2c85348d6b6e12`  
		Last Modified: Thu, 18 Dec 2025 02:19:47 GMT  
		Size: 86.0 MB (86020495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0233aa05e1bc12cff3808bd1a5019bd77b2ec5f562511d5c1ee34f12612d2c3`  
		Last Modified: Thu, 18 Dec 2025 02:19:39 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1335c7bdcbcf4ed5879d553c7bff9bfec64c6bb28cc526f8165157a3a4deac3`  
		Last Modified: Thu, 18 Dec 2025 02:20:09 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a83d91774852ead06e7a928e811e0f54c41dad64b3f74f2c7a4566c5397ba5f`  
		Last Modified: Thu, 18 Dec 2025 02:19:39 GMT  
		Size: 54.9 KB (54898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e268999278ddedbdce33b7af3a4d0ea12143ef8cc0ca605f9bfbdb1e5d4f4897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f876798b304cea567d45a4f4c36d063f1b804371d6a1679e066f0b0f1f8326d`

```dockerfile
```

-	Layers:
	-	`sha256:38d856e54e65779ecf73d1cd2b064905b7a7eadbec82b1b4806fd63364f2cff3`  
		Last Modified: Thu, 18 Dec 2025 03:20:06 GMT  
		Size: 11.3 MB (11342268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe6c6f298bb37a1d6eefa871010f2cd44b24795fe4d3f3d308d773497594a55`  
		Last Modified: Thu, 18 Dec 2025 03:20:08 GMT  
		Size: 20.9 KB (20881 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:d0c78633260e25523e8a59a3ef16da9e31618b81faf469c8e75e8c9ba1c3dd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.3 MB (444293241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d3d914fab78a1ee2e6feeda6302871fb33d7fe310ddf6d853e03a07ea1e455`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:03 GMT
ARG version=21.0.9.11-1
# Thu, 11 Dec 2025 22:11:03 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:11:03 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:11:03 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 11 Dec 2025 22:18:09 GMT
CMD ["gradle"]
# Thu, 11 Dec 2025 22:18:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 11 Dec 2025 22:18:09 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 11 Dec 2025 22:18:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 11 Dec 2025 22:18:09 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 11 Dec 2025 22:18:10 GMT
WORKDIR /home/gradle
# Thu, 11 Dec 2025 22:18:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 11 Dec 2025 22:18:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 11 Dec 2025 22:18:12 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 11 Dec 2025 22:18:12 GMT
USER gradle
# Thu, 11 Dec 2025 22:18:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 11 Dec 2025 22:18:13 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30afd867ba668143b0a83a28a417a56cea6bcf0208274f896e340f22161a864`  
		Last Modified: Thu, 11 Dec 2025 22:17:44 GMT  
		Size: 168.4 MB (168441547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c22c2927842f07fb3c529cadc014db4910fbc29964aa528ea5263ec89155376`  
		Last Modified: Thu, 11 Dec 2025 22:19:00 GMT  
		Size: 85.5 MB (85521851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c17c1294db9518fb80e4c65c2a4a255857dc0390165ba62930f187c291e3e5`  
		Last Modified: Thu, 11 Dec 2025 22:18:52 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb943702d2975507662397033f8e29245b7586f6503bccb0360e8d531e7fb97`  
		Last Modified: Fri, 12 Dec 2025 01:59:14 GMT  
		Size: 137.4 MB (137395176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8a447a2c21f25c3ad7c453e2e78de80caf7e50f7680d9c5d6341e859c0673a`  
		Last Modified: Thu, 11 Dec 2025 22:18:52 GMT  
		Size: 59.5 KB (59534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:724cf843253f7d9e6e40de7b8e4e2d5628a37226f85879b26f2e24110f11b4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11362300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa5cc6ff2c1d68dbc79da7ff784d8e44baf066c2ce3370adbea958918291d7e`

```dockerfile
```

-	Layers:
	-	`sha256:468557a50677220e6026d85a248897bfb0893c599c0a1b156f9133a841f159f5`  
		Last Modified: Fri, 12 Dec 2025 00:21:17 GMT  
		Size: 11.3 MB (11341246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3580f3ddf48a4f3d3cf0f45ca196b1cb856c7fef9945c3bd60e283866d86cb`  
		Last Modified: Fri, 12 Dec 2025 00:21:18 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
