## `gradle:9-jdk17-corretto`

```console
$ docker pull gradle@sha256:9c9ce251f5fddea3b6ff27679eeb00e90ae869af004c2b5d8e92a581d009398d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:7c88d4742af7c9264bda94bd2abb2c87c1800aaa508c545140d58bd4a456e7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.8 MB (434849600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0e0b47eb98360f29961db7e61eeb778447d5546ddda14f74b613952a59d9b73`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:18 GMT
ARG version=17.0.18.9-1
# Wed, 11 Mar 2026 18:33:18 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:33:18 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:33:18 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 20 Mar 2026 17:11:27 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:11:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:11:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Mar 2026 17:11:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 17:11:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:11:28 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:11:28 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:11:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:11:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:11:30 GMT
USER gradle
# Fri, 20 Mar 2026 17:11:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:11:31 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055cd026c36d762ae8609c747f4ea79d2a9e6706090e299a5680a5250aa1887b`  
		Last Modified: Wed, 11 Mar 2026 18:33:38 GMT  
		Size: 156.9 MB (156911233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2592eead4d9acfe7147fe1ea180c0ed469d029c8d10ecefbb12fcc4a768438f8`  
		Last Modified: Fri, 20 Mar 2026 17:12:04 GMT  
		Size: 86.1 MB (86069660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a686cce810ed5f7d700b58e74dd386414fb40f08da9b7e5c26f1faf02da717`  
		Last Modified: Fri, 20 Mar 2026 17:11:59 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107eb8cba46e41197707e9b1624ca8322d6b8ef634834dc0a64423d07a2997b6`  
		Last Modified: Fri, 20 Mar 2026 17:12:04 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b2ec3861585c04824bf1ff6c10acd4b20de8a8fbe944715ca42a938ca004f5`  
		Last Modified: Fri, 20 Mar 2026 17:11:59 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:62c3e12c60b4eb45c67ac1c8b661880e1f5381323d2d146a03b45003318a8017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11347829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b97ddbd75a48938ed74ddaac82abc0ea522fac88d86a8a1c1131646e10b2576`

```dockerfile
```

-	Layers:
	-	`sha256:8f6b20074d76cfc7d86c828b7aee70c97571896c08476814a2c2e3f3b7ada53d`  
		Last Modified: Fri, 20 Mar 2026 17:12:00 GMT  
		Size: 11.3 MB (11326332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9228fb9265ca8d9739e9dbd6098201427bac407e48e4a2c2549db79c409025c`  
		Last Modified: Fri, 20 Mar 2026 17:11:59 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:071cd7668334e950d167dfdf49ac92a41715778970bcd19e597cb957b96dd9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.1 MB (432053418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc33324dab81dcf169854036c7b97f65eddd7b111238f13a75f26da3f27e60d7`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:16 GMT
ARG version=17.0.18.9-1
# Wed, 11 Mar 2026 18:33:16 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:33:16 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:33:16 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 20 Mar 2026 17:11:16 GMT
CMD ["gradle"]
# Fri, 20 Mar 2026 17:11:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 20 Mar 2026 17:11:16 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 20 Mar 2026 17:11:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 20 Mar 2026 17:11:16 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 20 Mar 2026 17:11:16 GMT
WORKDIR /home/gradle
# Fri, 20 Mar 2026 17:11:16 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 20 Mar 2026 17:11:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 20 Mar 2026 17:11:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 20 Mar 2026 17:11:19 GMT
USER gradle
# Fri, 20 Mar 2026 17:11:20 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 20 Mar 2026 17:11:20 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad03905648f3b93bd27022168e0d020ec9500985cd24049dda94b8aa0d74f58`  
		Last Modified: Wed, 11 Mar 2026 18:33:39 GMT  
		Size: 155.7 MB (155727845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149cb219f0cc1f09b365865875506d147a69e780d527f2e2d8c17b73b409b146`  
		Last Modified: Fri, 20 Mar 2026 17:11:50 GMT  
		Size: 85.5 MB (85544854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d06abbd23c4e5a4c61a23eb0ef3161b2721c16a50decb10a75a8ac09e318d6`  
		Last Modified: Fri, 20 Mar 2026 17:11:47 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ca52dea1251946f9f1d8b0a1b8565f0c8d7ec50e65845ec64d95e825c4cb14`  
		Last Modified: Fri, 20 Mar 2026 17:11:51 GMT  
		Size: 137.8 MB (137808333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0d28332ed1cadbd9866aa5beec46da459a2ecf344a6aa6ca3ab8edd5834ab9`  
		Last Modified: Fri, 20 Mar 2026 17:11:47 GMT  
		Size: 29.3 KB (29329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:4dc357c8fc3c061f3ed29076420e1d30216d6e8666e6df4258729a0cd253c227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11347024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f98f3a3e127e5d2aa1053ed9d6de3008ad325ce96f99da78b6bda0c85c91a16`

```dockerfile
```

-	Layers:
	-	`sha256:3c11872dc0b259442a7c951a280b6b062e14add7d110bf2f9332773df58c7769`  
		Last Modified: Fri, 20 Mar 2026 17:11:48 GMT  
		Size: 11.3 MB (11325331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f979cdd05c6dd644a20fa2a4c3aceda510860757853ca6813abeef112537699`  
		Last Modified: Fri, 20 Mar 2026 17:11:47 GMT  
		Size: 21.7 KB (21693 bytes)  
		MIME: application/vnd.in-toto+json
