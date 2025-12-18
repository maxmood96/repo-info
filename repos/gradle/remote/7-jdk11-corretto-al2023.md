## `gradle:7-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:b65e801f2126872e0ab485c6a7bb88c013c63986052dc2acaa989f779aeb076a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:7021cf2beb36bdd6a1ecdcafc82855e313e7a891c6803420c54ebee1af00b20a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.9 MB (421850851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d391aff2a9be7870e6e00478b9ff54c4cc5366791d3289ec4e05c621886b18`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:17:42 GMT
ARG version=11.0.29.7-1
# Thu, 18 Dec 2025 01:17:42 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:17:42 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:17:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 18 Dec 2025 02:19:25 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:19:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:19:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:19:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:19:25 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:19:25 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:19:25 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 18 Dec 2025 02:19:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 18 Dec 2025 02:19:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:19:27 GMT
USER gradle
# Thu, 18 Dec 2025 02:19:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Dec 2025 02:19:28 GMT
USER root
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922be8b112d0964cf5a32536184dc5a2757f1733ff0abfcd1dd0bb1839afb6fa`  
		Last Modified: Thu, 18 Dec 2025 01:18:18 GMT  
		Size: 153.3 MB (153314360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e74840989cff3ca92da28b4ce996cbb535f3525a3c59ef486ccf2d22403de4b`  
		Last Modified: Thu, 18 Dec 2025 02:20:14 GMT  
		Size: 86.0 MB (86022028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af83555761d7fa14dc0b0d349fbb87a5f10ca980e1aef437acd0660b1600cafd`  
		Last Modified: Thu, 18 Dec 2025 02:20:07 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd160df77e883d7f370d9c1a98838e5df7fe2344f754ee405f7f4101f128d609`  
		Last Modified: Thu, 18 Dec 2025 02:20:31 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3eaa0157942a0a58071dc9b0ad2f97221058271d3b419d63d3fd8d579e9a430`  
		Last Modified: Thu, 18 Dec 2025 02:20:07 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:469bff1f3e3dd0705db5b71eeaea1a5dddb8ed058b3dd1c66f6a65efd5ea0fa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11296842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa292ff4dd243ca41a200541aebf8525c584fdec3af0b7bc6f34fa77226d636f`

```dockerfile
```

-	Layers:
	-	`sha256:6bcd5c7ffb2b9af22e2c9b4fee9b7737e42db3029ec8b3bcc35ad1fdd44e967b`  
		Last Modified: Thu, 18 Dec 2025 06:18:31 GMT  
		Size: 11.3 MB (11275971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c40022d848476074b0c04177a49d36d55e142d52798aa8b15001af3866b8efea`  
		Last Modified: Thu, 18 Dec 2025 06:18:32 GMT  
		Size: 20.9 KB (20871 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:aa0c32a0bae5612d82346c1ee50f3e8f8ad30f8b87f70af737864ff08c4f5d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.8 MB (418787421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead8beacaa82c9ca976daebec12e8d30d2f04c445a344dbaecb8791158789c54`
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
# Thu, 18 Dec 2025 02:19:45 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:19:45 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:19:45 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:19:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:19:45 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:19:45 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:19:45 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 18 Dec 2025 02:19:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 18 Dec 2025 02:19:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:19:48 GMT
USER gradle
# Thu, 18 Dec 2025 02:19:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Dec 2025 02:19:48 GMT
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
	-	`sha256:e824e073cc9fd808a0f87367fe590c06d3698d9072c58114fc10cf5d20389d5e`  
		Last Modified: Thu, 18 Dec 2025 02:20:36 GMT  
		Size: 85.5 MB (85525459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a644fb64f30d2550076019e5bdfe785c91008fe793bc54f16aae379f87cc9d22`  
		Last Modified: Thu, 18 Dec 2025 02:20:28 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f828f35a8ff26db091688afc06005eac0b502c01ee679fcac84efcd81a906f`  
		Last Modified: Thu, 18 Dec 2025 02:20:21 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ae5f3bf288c6263a20cb6dd73329a9d19cde27bdb158b2c1f961a38fcee291`  
		Last Modified: Thu, 18 Dec 2025 02:20:28 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:2a93a3b1e675de9a59e14d24a361a40a20398a2eca74f693cda72026f6f8f432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11296834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852f4007f27c02fd5435e1b90b96f1751410436102ee5ba9727287396498d467`

```dockerfile
```

-	Layers:
	-	`sha256:293b0c80383c5f3c170e76a9cec7627a5c773ff670dd166a5ed44428bb45d921`  
		Last Modified: Thu, 18 Dec 2025 03:19:15 GMT  
		Size: 11.3 MB (11275790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e02d7746564ba38f99e098887ad268ae6d17659d843daaf02e2db8d655a51b5`  
		Last Modified: Thu, 18 Dec 2025 03:19:16 GMT  
		Size: 21.0 KB (21044 bytes)  
		MIME: application/vnd.in-toto+json
