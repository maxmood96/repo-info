## `gradle:8-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:3a1084990c2de28399b7f59736f3e83f1a9a1201c3ea5cf539abdf5b7ce6b0b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:b1e64bdaea3b8b7a99d2eaffcc4c39fb36e33f0b1bec77fd1534c9d9f3d172ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.8 MB (430828829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2fd28bd123a235d8a94144afb03b1d9e911fa90834d5716abbdec720558af9`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:41 GMT
ARG version=11.0.29.7-1
# Thu, 15 Jan 2026 22:09:41 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:09:41 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:09:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 15 Jan 2026 23:08:33 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 23:08:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 23:08:33 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 23:08:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 23:08:33 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 23:08:33 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 23:08:33 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 15 Jan 2026 23:08:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 15 Jan 2026 23:08:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 23:08:35 GMT
USER gradle
# Thu, 15 Jan 2026 23:08:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 23:08:36 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d80e849e0986824104f94780e496e5f0b7ca3decbfc934b6f1ee3b8406bd6c8`  
		Last Modified: Thu, 15 Jan 2026 22:10:20 GMT  
		Size: 153.3 MB (153314830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28594fd6cc963bde8497907f028ea166365a4e4ea10a37f21a7764f2599030d9`  
		Last Modified: Thu, 15 Jan 2026 23:09:37 GMT  
		Size: 86.0 MB (86041003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4691b61303bb1d36ca8f0c67109d5fd9e98e4cea7c63cb65ff5b33586a73bfc3`  
		Last Modified: Thu, 15 Jan 2026 23:09:16 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8308b4cb47caba0e817c6dba02b9c9e6f865620ea911958e53de1ec859b8edf7`  
		Last Modified: Fri, 16 Jan 2026 00:32:44 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ef4f06f586b20c2aade4f3ed324ba10e4c0c211715a06794d1b921f1e8ea7`  
		Last Modified: Thu, 15 Jan 2026 23:09:16 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a7ae748193723c49437cc22990745de55da1e3429e8dd0c48438c2cef8ab2884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7cdbfc9decb6a498a163c4ad25765e6f8ff769dd68b067b2992ee0ef51b143`

```dockerfile
```

-	Layers:
	-	`sha256:f5ba262e0e6b1c05f1792817825cb06e69739eaf6373bf7c3cd74c1e69fa1994`  
		Last Modified: Fri, 16 Jan 2026 00:26:29 GMT  
		Size: 11.4 MB (11366000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3963dc3179a76c4296e3e811fb7e670baa88c05028cb7a255855ffa40f09dc13`  
		Last Modified: Fri, 16 Jan 2026 00:26:35 GMT  
		Size: 21.5 KB (21523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e7630f9b9da07c9b25c7b103e5d0ae66d11da235aee333f8b8f87955c42d6004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.7 MB (427712930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d70e83a95650c8478a8759487789d3059d4ac82000922ed308563e7a04747d`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:25:36 GMT
ARG version=11.0.29.7-1
# Thu, 18 Dec 2025 01:25:36 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:25:36 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:25:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 18 Dec 2025 02:19:40 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:19:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:19:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:19:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:19:40 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:19:40 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:19:40 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 18 Dec 2025 02:19:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 18 Dec 2025 02:19:43 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:19:43 GMT
USER gradle
# Thu, 18 Dec 2025 02:19:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Dec 2025 02:19:44 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d97a22c455e699058453c0de8fe96a1082e1e0c45147a1b31b1c201d708c82`  
		Last Modified: Thu, 18 Dec 2025 01:26:28 GMT  
		Size: 151.9 MB (151857883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87614a92f5a2513ea7686532ba25f0754a86fbbd154e15b9f24ad9ea245a3f89`  
		Last Modified: Thu, 18 Dec 2025 02:20:33 GMT  
		Size: 85.5 MB (85525188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7f4b68b4005818834ce70329fb9b2852e70ce4a21274f8dc3f563fb7f58643`  
		Last Modified: Thu, 18 Dec 2025 02:20:23 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeba2868f0127e5ec7fcd3c1b9ed3a943966e468142eb8aed4bcfe1a5ae3c96f`  
		Last Modified: Thu, 18 Dec 2025 02:20:41 GMT  
		Size: 137.4 MB (137395193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96693bfa8adee18b053b7c1cbdb556c7aeed479b018788c6f1fd24947fb68dd6`  
		Last Modified: Thu, 18 Dec 2025 02:20:23 GMT  
		Size: 59.5 KB (59537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:94f741e537ea9f602d013a0da3f3558b1fd3a98e858c9d139a9dca45bd49cd47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d710a89caaa4b42b10ef5d55a778761ab8dc21399a5c5bf95b128ba817a403`

```dockerfile
```

-	Layers:
	-	`sha256:8fdc0983c2a70a9b5f30695ab48a5fb0b75a2a220dfc52483c4a091c971c206e`  
		Last Modified: Thu, 18 Dec 2025 03:19:55 GMT  
		Size: 11.4 MB (11365839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0d0a1e4652a3f8debf50e19df57aabe2ffdeb6675806b07511abdb273a8e805`  
		Last Modified: Thu, 18 Dec 2025 03:19:56 GMT  
		Size: 21.7 KB (21720 bytes)  
		MIME: application/vnd.in-toto+json
