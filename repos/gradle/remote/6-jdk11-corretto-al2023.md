## `gradle:6-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:470f2132556eee3bd021133b080ce01e1c118d55b6a122dbfc1671e21e3390b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:c17661b189738870f82f4dbf2da18057fd507d477f4d68b4d7446dd703833865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 MB (401099508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:889d2d40e7a701edb14b8e583f198633e87fb4be16c55a81fbe085e198bbc741`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:25 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:11:25 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:11:25 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 31 Oct 2025 01:12:33 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:12:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:12:33 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:12:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:12:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:12:33 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:12:33 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 31 Oct 2025 01:12:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 31 Oct 2025 01:12:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:12:35 GMT
USER gradle
# Fri, 31 Oct 2025 01:12:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:12:36 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f643f97c106e8b010a5e3ab951bd53f9b0f08ee366ac0330e4641b14e18fa31`  
		Last Modified: Fri, 31 Oct 2025 01:11:37 GMT  
		Size: 153.3 MB (153345023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937f47d43786fec252010f4f0b5def85aee87273fbe5f68577c90fb257e6b4fd`  
		Last Modified: Fri, 31 Oct 2025 01:13:32 GMT  
		Size: 85.6 MB (85623667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4b4ff5f5839bce6b2d4d5cce0719fb5b5d6b13233131ad0db93e00dfa3ca69`  
		Last Modified: Fri, 31 Oct 2025 01:13:21 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdaa0e5eb957d27a8b4b1a9a5f3b02c36ff8fd8bd1714aa7b3de44ec9be36cfe`  
		Last Modified: Fri, 31 Oct 2025 01:13:32 GMT  
		Size: 107.7 MB (107696633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6884b516dc169bb968f1718c258777ffb6388e9db87da1c16b693bc1cca1b91d`  
		Last Modified: Fri, 31 Oct 2025 01:13:21 GMT  
		Size: 431.3 KB (431269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:b93b46d107d2645c549d21e087304f4ab8d4872cfb04331e6a8ec30cd1f8d091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11257563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc36f4ea6560483af291b0853354c24c082075339d50d09da9b3c1dca67fe1a6`

```dockerfile
```

-	Layers:
	-	`sha256:4b4b02d3dd13b60ae72ec048c62910b5c28afb70b39a95a5344903f789e45fc1`  
		Last Modified: Fri, 31 Oct 2025 02:17:26 GMT  
		Size: 11.2 MB (11236691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61acaf8b54bb9693d21e6b674f1d61516ed1613a56e2e1b95a9649f345f2dfcf`  
		Last Modified: Fri, 31 Oct 2025 02:17:26 GMT  
		Size: 20.9 KB (20872 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bd932f856432ccc7388fc7000c27e10743bded3422873370d3262c366d48ef06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.1 MB (398082344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d308521ef9680c98d27b5a560e5c7139cf03a6ea9475a6caa1db1492f886efb6`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:29 GMT
ARG version=11.0.29.7-1
# Thu, 06 Nov 2025 22:13:29 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:13:29 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 06 Nov 2025 23:13:15 GMT
CMD ["gradle"]
# Thu, 06 Nov 2025 23:13:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Nov 2025 23:13:15 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Nov 2025 23:13:15 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Nov 2025 23:13:15 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Nov 2025 23:13:15 GMT
WORKDIR /home/gradle
# Thu, 06 Nov 2025 23:13:15 GMT
ENV GRADLE_VERSION=6.9.4
# Thu, 06 Nov 2025 23:13:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Thu, 06 Nov 2025 23:13:18 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Nov 2025 23:13:18 GMT
USER gradle
# Thu, 06 Nov 2025 23:13:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Nov 2025 23:13:19 GMT
USER root
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f1158d8b36acddc8839ac2d61ff7da04401b085f3c33c4996bbdc4d1e0ea8a`  
		Last Modified: Thu, 06 Nov 2025 23:12:11 GMT  
		Size: 151.9 MB (151892114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa55e5951a2c89a9e4fe7327d20827240e5ac13623295da7b9cd8d8bdcef60b`  
		Last Modified: Thu, 06 Nov 2025 23:14:04 GMT  
		Size: 85.2 MB (85165176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615ee67f8a8462fe19b2b612c6cd046a290adafb018c71405954897b63bb7197`  
		Last Modified: Thu, 06 Nov 2025 23:13:55 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbaf4c83d05e8ecbd31c4a4533d41bd9d62c5fadc031e7dbfe2566b120d35fcd`  
		Last Modified: Thu, 06 Nov 2025 23:14:15 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e230431d43f1a196007e93454c945f95a802ac2853aa84e3b3bf31012555901`  
		Last Modified: Thu, 06 Nov 2025 23:13:58 GMT  
		Size: 425.0 KB (425024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:4a9c90b07182e29ffadf5ec0bb3f1e89cb6226067392686279e39b9bdd493b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11257555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f9df30b8b51770b606c31d0cec9a3d721f59c24807c5ee5cd0844b081bc235`

```dockerfile
```

-	Layers:
	-	`sha256:4e084078495dcb00d5e8b9ad3eecb914f47f540d6c330c46e0b9b3f4a3b7e0f5`  
		Last Modified: Fri, 07 Nov 2025 00:17:36 GMT  
		Size: 11.2 MB (11236510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e2756314176cfa451b0253b2eb6e656740a55eb2ba34a678895e806a9d83f24`  
		Last Modified: Fri, 07 Nov 2025 00:17:37 GMT  
		Size: 21.0 KB (21045 bytes)  
		MIME: application/vnd.in-toto+json
