## `gradle:8-jdk11-corretto`

```console
$ docker pull gradle@sha256:f6694fa6a0a58e9924918abc37e0a15b16a3b67aff8624e3ec3d099afa5494bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto` - linux; amd64

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
		Last Modified: Thu, 15 Jan 2026 22:10:03 GMT  
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
		Last Modified: Thu, 15 Jan 2026 23:09:11 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52ef4f06f586b20c2aade4f3ed324ba10e4c0c211715a06794d1b921f1e8ea7`  
		Last Modified: Thu, 15 Jan 2026 23:09:16 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

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

### `gradle:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6e2c2a93588fe28e8f926816338ff0c3a1df5ee73b3a3628ec882ffc8aa22992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.8 MB (427751395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f800d149cd3e34a35a4a238ec892766703f7e375c17b9728a2818563eef95ac`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:34 GMT
ARG version=11.0.29.7-1
# Thu, 15 Jan 2026 22:08:34 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:08:34 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 15 Jan 2026 23:15:44 GMT
CMD ["gradle"]
# Thu, 15 Jan 2026 23:15:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 15 Jan 2026 23:15:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 15 Jan 2026 23:15:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 15 Jan 2026 23:15:44 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 15 Jan 2026 23:15:44 GMT
WORKDIR /home/gradle
# Thu, 15 Jan 2026 23:15:44 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 15 Jan 2026 23:15:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 15 Jan 2026 23:15:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 15 Jan 2026 23:15:47 GMT
USER gradle
# Thu, 15 Jan 2026 23:15:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 15 Jan 2026 23:15:47 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb516caff5975026fd4cb1685b25ef916ac594c49bf6ec816847c2506e060df`  
		Last Modified: Thu, 15 Jan 2026 22:08:56 GMT  
		Size: 151.9 MB (151859277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce609b282fe5642b19943c1215695074e03b3ae26e9e0189468e18680a65b14`  
		Last Modified: Thu, 15 Jan 2026 23:16:18 GMT  
		Size: 85.5 MB (85521354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5e2d93febcd40a3d734fdc1b0e3f1c4ed59267c03041e1f3ec38dc06ca60fb`  
		Last Modified: Thu, 15 Jan 2026 23:16:26 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e38f36dce503f5382cd5443aac7e524c98d376b7c07d9e2ff32fd775ade4db`  
		Last Modified: Thu, 15 Jan 2026 23:16:19 GMT  
		Size: 137.4 MB (137395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a062e420c3bd2120c38917cb1c40dff7e4f54731e2e7bac69e45154514ab7a8`  
		Last Modified: Thu, 15 Jan 2026 23:16:25 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:803b2563e26d4f67ce0a0a8babab9ab1c28bcd2cccd7e7eb03ea8022a32a9899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babc97d7e3c753444988d4fd85f4e8257b97dcc31620ca57d8028c77db7e8557`

```dockerfile
```

-	Layers:
	-	`sha256:7e0d75f718841cf458489b05536b9d62cccb397c4416fe4c7e979fb24a39872b`  
		Last Modified: Fri, 16 Jan 2026 00:29:28 GMT  
		Size: 11.4 MB (11365843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f665783c8aa65c4fc2c5d657c181361ca613307b53ab4cfe4f8e23d5050d27`  
		Last Modified: Fri, 16 Jan 2026 00:29:29 GMT  
		Size: 21.7 KB (21720 bytes)  
		MIME: application/vnd.in-toto+json
