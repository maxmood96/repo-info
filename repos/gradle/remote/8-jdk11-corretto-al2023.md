## `gradle:8-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:62a8128173f7636d6b16cedf244aa48fe9b9eff38875ed174ca7769dff601b5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:a0cc49a0803d43a8e4ec3d68648b782ed9ea822f55ec34b6535c5e9862cc9b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.8 MB (430777341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736f6f95e8b81511a1b738032c05463fc8332162f2727857eeb6e4685d38ffa2`
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
# Thu, 18 Dec 2025 02:19:02 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:19:02 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:19:02 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:19:02 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:19:02 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:19:02 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:19:02 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 18 Dec 2025 02:19:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 18 Dec 2025 02:19:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:19:04 GMT
USER gradle
# Thu, 18 Dec 2025 02:19:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Dec 2025 02:19:05 GMT
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
	-	`sha256:074f08b001644f7e5c636fa896d0e06a1e6c74a8203bc9613dbe49ce6842f0ae`  
		Last Modified: Thu, 18 Dec 2025 02:19:44 GMT  
		Size: 86.0 MB (86022739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13920272a6ad46fdc846d05b54ce2f87ed8508b9d169be1bdbf540f51bd47794`  
		Last Modified: Thu, 18 Dec 2025 02:19:39 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a5e8abb34334e4d9af7a1555359e34eaec44d106a253c33e0ba2f7de18b932`  
		Last Modified: Thu, 18 Dec 2025 02:19:55 GMT  
		Size: 137.4 MB (137395201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab12275d6bffaa3e636ca5d22b29a5fea83163a13dbd0deb3af8e08510f8ae12`  
		Last Modified: Thu, 18 Dec 2025 02:19:39 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:123285161bba2effde39baa10fff96e4f9575e7edd96ee455e9bd55352e84d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ca6db94826a2b9ff6bae20a7e5b1762d25bf78ca9064c79f6f219f9ddd5c9e`

```dockerfile
```

-	Layers:
	-	`sha256:3422a1bb70f1c0321bf2e0d113cb51ce13ba4bd4e0c6828f02d3d7851556dd46`  
		Last Modified: Thu, 18 Dec 2025 03:19:45 GMT  
		Size: 11.4 MB (11365996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb94bce4577972ae56870db33834126578aa655a2c03619347c205911efb386`  
		Last Modified: Thu, 18 Dec 2025 03:19:46 GMT  
		Size: 21.5 KB (21523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:25f5ab26af46613f4eb046e1443b505325a5bd5fca567e827602dce5144e9478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.7 MB (427711938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f7ef61b5c3e0c0754bde7bd8bd6337862e5f068d886324c19af90df7e6c2ec`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:45 GMT
ARG version=11.0.29.7-1
# Thu, 11 Dec 2025 22:11:45 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:11:45 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 11 Dec 2025 22:17:23 GMT
CMD ["gradle"]
# Thu, 11 Dec 2025 22:17:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 11 Dec 2025 22:17:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 11 Dec 2025 22:17:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 11 Dec 2025 22:17:23 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 11 Dec 2025 22:17:23 GMT
WORKDIR /home/gradle
# Thu, 11 Dec 2025 22:17:23 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 11 Dec 2025 22:17:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 11 Dec 2025 22:17:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 11 Dec 2025 22:17:25 GMT
USER gradle
# Thu, 11 Dec 2025 22:17:26 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 11 Dec 2025 22:17:26 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87007ffe7b7b13cd2a1a2beb82088f869ecda44267275742bf5382df619ea96a`  
		Last Modified: Thu, 11 Dec 2025 22:12:25 GMT  
		Size: 151.9 MB (151857944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9f0312b5bbfc9c90e41be923353c23b8468dc031dab0e25c979887f3a0739dc`  
		Last Modified: Thu, 11 Dec 2025 22:18:14 GMT  
		Size: 85.5 MB (85524140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10790059966b526c288235038ec6bcdca2b24f2d0424f062c11ad5bc3bdb1cb`  
		Last Modified: Thu, 11 Dec 2025 22:18:04 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c151c2b69a24ea3ca601f35025821975abe17b08ccfd22e61aeb8ff2f1ed4dce`  
		Last Modified: Fri, 12 Dec 2025 02:52:44 GMT  
		Size: 137.4 MB (137395192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7c0128e120a92c97254f46958d353d22f12eaffd081d2df86272ba9fe95869`  
		Last Modified: Thu, 11 Dec 2025 22:18:04 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:9c296a285d0c2cd23b624cab8e72d62dcff49d879413bae8552a3b257812169c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d882955373bc8c761fe79f736412b07e048766a29e93c946e40583986922c34`

```dockerfile
```

-	Layers:
	-	`sha256:cca911820733a1a0bda417635886d8c1b02437c9069dc3c68796b92ee39406e8`  
		Last Modified: Fri, 12 Dec 2025 00:20:46 GMT  
		Size: 11.4 MB (11365839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9080bf59629b2771544fcfbe7ae467af7667e574c75899e660f6535fd769ab1b`  
		Last Modified: Fri, 12 Dec 2025 00:20:47 GMT  
		Size: 21.7 KB (21720 bytes)  
		MIME: application/vnd.in-toto+json
