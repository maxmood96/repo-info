## `gradle:8-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:baedf480a6604a9c5a3fa5d60e70790f1655e0fc388f4e255a9c5798882e7494
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:c8e86883088ddf9b742fc06163931b11691c39ccd2dcb62ca90f348d2f0e3a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.3 MB (587300409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fe276b19213b5a99a1f0e3106bf68776b163b33e7a6c1b5c40c5409a68be2e`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:25 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:11:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:11:25 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 31 Oct 2025 01:12:18 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:12:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:12:18 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:12:18 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:12:18 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:12:18 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:12:18 GMT
ENV GRADLE_VERSION=8.14.3
# Fri, 31 Oct 2025 01:12:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Fri, 31 Oct 2025 01:12:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:12:21 GMT
USER gradle
# Fri, 31 Oct 2025 01:12:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:12:21 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d90a02718a2ec471735b22a7012a63f3b6fd6aa7b11464ff1edf280a2e204b8`  
		Last Modified: Fri, 31 Oct 2025 01:12:00 GMT  
		Size: 330.9 MB (330868176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1b51de5e0fe96e4f5332f1ee6221a29cae2db99d9aa669b21557255cf38ebd`  
		Last Modified: Fri, 31 Oct 2025 01:13:28 GMT  
		Size: 65.0 MB (64978988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776f2587e620e18d16b56418da43ed9c516dc8a243a658f5ef2a34c3b2337814`  
		Last Modified: Fri, 31 Oct 2025 01:13:22 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429f0a9d5dc7116a8bde327f75e32a42c446041b3eca82145b4151a8f6670381`  
		Last Modified: Fri, 31 Oct 2025 02:34:38 GMT  
		Size: 137.4 MB (137395131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9ffbd829ba973c7e7a8737f736fe0e9f87788f87786fed3758b60e5199284a`  
		Last Modified: Fri, 31 Oct 2025 01:13:22 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:7afd019e216f761df674cdd52ee9cbb64a786fdeaebb64fb03f189080352288a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18154003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e304ab2d6f5f27010e787cac1347b107339697aa38d7fd5a25201360441ace`

```dockerfile
```

-	Layers:
	-	`sha256:768916fbeaec25d9b614fddc72bdfbddb66ca65fb985add64f6434726f836d4b`  
		Last Modified: Fri, 31 Oct 2025 02:21:14 GMT  
		Size: 18.1 MB (18132487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e7b269bd56104dadf5e60c0313a8b7772f1f081fb088b48cb1b2907cbb76eed`  
		Last Modified: Fri, 31 Oct 2025 02:21:15 GMT  
		Size: 21.5 KB (21516 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c0a2fabba942bd5698ac71b105c3b557a0f8a3845efdff8a3e823f526f9b942c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.5 MB (393469633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ac27d265e478b0ab3650863ff8ae1854d9a7efbb53591f6092a0a311346a11`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:43 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:11:43 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:11:43 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 31 Oct 2025 01:12:27 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:12:27 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:12:27 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:12:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:12:27 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:12:27 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:12:27 GMT
ENV GRADLE_VERSION=8.14.3
# Fri, 31 Oct 2025 01:12:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Fri, 31 Oct 2025 01:12:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:12:30 GMT
USER gradle
# Fri, 31 Oct 2025 01:12:30 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:12:30 GMT
USER root
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d388cefb5877034eb46c74035ba24455c55fff50dbbe8d7c47526c4022768c`  
		Last Modified: Fri, 31 Oct 2025 01:12:01 GMT  
		Size: 118.0 MB (117956928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f666361f19e881e562559a1e8cc87ee05af7b5b32b9ca4fc5c4ba7879b3d76e`  
		Last Modified: Fri, 31 Oct 2025 01:13:22 GMT  
		Size: 85.2 MB (85154514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c645f768d8f9b9b5f5a5d996b880239684f7987cf0fe6570e1ae59b5150d2bd`  
		Last Modified: Fri, 31 Oct 2025 01:13:08 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47f327c2e5836a5f2c55a354e65658efb7e8d045ad93ef8e1e1e2321e07706e`  
		Last Modified: Fri, 31 Oct 2025 01:13:03 GMT  
		Size: 137.4 MB (137395131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b72997dea01f310e0577d4e9b7fa301b8fbbb44daa13597471c029af8bb04a`  
		Last Modified: Fri, 31 Oct 2025 01:13:08 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a7dc1d47675f956e8642a2d53b3f3a0d52acd171436837bb5301bb98329197bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11718390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81abe04701d582205ed29f28650265330e76bf7c4e77d7beda1ffb1fee3aec99`

```dockerfile
```

-	Layers:
	-	`sha256:755f61baee315862331ee9557641912a04bd01d5d0dac5a140c2812c24b6bb12`  
		Last Modified: Fri, 31 Oct 2025 02:21:30 GMT  
		Size: 11.7 MB (11696677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a18d10eaaa3c954d93cd111174b4a9301fcc5c29d013e71eb735d25890e523e`  
		Last Modified: Fri, 31 Oct 2025 02:21:31 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json
