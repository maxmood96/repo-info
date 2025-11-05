## `gradle:9-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:59cfcd4c1bfd971e928d36c435a302dd765fea580f1d866f60f42e11646fdb71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:9cb28955cadf1108a171d104645c00a063c85757d6e2530bc52c1bdf52734a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.4 MB (445409568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55680a149b7c8527552006b6b8d6dd474251a2aed49614cc79b104a1d7fc5a56`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Wed, 05 Nov 2025 01:06:16 GMT
ARG version=21.0.9.11-1
# Wed, 05 Nov 2025 01:06:16 GMT
ARG package_version=1
# Wed, 05 Nov 2025 01:06:16 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 05 Nov 2025 01:06:16 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 05 Nov 2025 04:50:28 GMT
CMD ["gradle"]
# Wed, 05 Nov 2025 04:50:28 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 05 Nov 2025 04:50:28 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 05 Nov 2025 04:50:28 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 05 Nov 2025 04:50:28 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 05 Nov 2025 04:50:28 GMT
WORKDIR /home/gradle
# Wed, 05 Nov 2025 04:50:28 GMT
ENV GRADLE_VERSION=9.2.0
# Wed, 05 Nov 2025 04:50:28 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Wed, 05 Nov 2025 04:50:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 05 Nov 2025 04:50:31 GMT
USER gradle
# Wed, 05 Nov 2025 04:50:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 05 Nov 2025 04:50:31 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d298c96cc089701668f1f26ebc2ed62153aa52cd816ed6691a3e4aa37f8b318`  
		Last Modified: Wed, 05 Nov 2025 02:50:01 GMT  
		Size: 170.2 MB (170217752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dec9a7d121d993e74c7c75ec515470fdcb46e749ada6b2d0e373487e7ecf7f0`  
		Last Modified: Wed, 05 Nov 2025 04:51:24 GMT  
		Size: 85.6 MB (85612342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7c8838f3694f04837b7186addd6cec45ce2b69f9e473f1223c9cd98f960782`  
		Last Modified: Wed, 05 Nov 2025 04:51:11 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8a89218902a7b0a924ca0f2f1a09e229993009d1703612b28f7b33987c09e1`  
		Last Modified: Wed, 05 Nov 2025 06:33:40 GMT  
		Size: 135.5 MB (135521661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc4cc3ec06274cf705cfce87a7fad984eed7eb624ad1386713aaa8d7460985f`  
		Last Modified: Wed, 05 Nov 2025 04:51:11 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:113fb8eaaa27641d9032b8e6a128b9287ca58aa6321be2b304d5aa3473be3bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11337374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d499a0589e18b06235a58966b782dcbb26a82c1ce4e44fd36133f88b4b9013`

```dockerfile
```

-	Layers:
	-	`sha256:4688b2437c7cf8c8ed4b23d9caf7887df46c8f512b7275fc45b9fded93b7079a`  
		Last Modified: Wed, 05 Nov 2025 06:21:16 GMT  
		Size: 11.3 MB (11315772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d62c2bbad74cda26f51c18daa8d15884048b80c5e01d1ab8f56ec3353d775c0b`  
		Last Modified: Wed, 05 Nov 2025 06:21:16 GMT  
		Size: 21.6 KB (21602 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:4fa78d125e5c5c864b36c0a369faaa6ab8db36b32a48437bccef44ba80ddd549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.1 MB (442127794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ef842cba841c5f913dbb7b1c5c5d24e6cfe8a25895c7987715524912cbd16a`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:13:20 GMT
ARG version=21.0.9.11-1
# Tue, 04 Nov 2025 23:13:20 GMT
ARG package_version=1
# Tue, 04 Nov 2025 23:13:20 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Nov 2025 23:13:20 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:13:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 04 Nov 2025 23:26:00 GMT
CMD ["gradle"]
# Tue, 04 Nov 2025 23:26:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Nov 2025 23:26:00 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Nov 2025 23:26:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Nov 2025 23:26:01 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Nov 2025 23:26:01 GMT
WORKDIR /home/gradle
# Tue, 04 Nov 2025 23:26:01 GMT
ENV GRADLE_VERSION=9.2.0
# Tue, 04 Nov 2025 23:26:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Tue, 04 Nov 2025 23:26:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Nov 2025 23:26:04 GMT
USER gradle
# Tue, 04 Nov 2025 23:26:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Nov 2025 23:26:04 GMT
USER root
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c2727794d09d1991e86e7be4460efa70d877f3e2f01e42868f86a28a40c4a3`  
		Last Modified: Tue, 04 Nov 2025 23:25:36 GMT  
		Size: 168.5 MB (168474625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb15984bdadb39f94c727b967fd539ffa20b1a136ccb7668c04bdd1425a44ee`  
		Last Modified: Tue, 04 Nov 2025 23:27:02 GMT  
		Size: 85.2 MB (85168379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c9ae096851145b4456c4889b1cb1841d56af870e8c08ba5dbd469e13874cf7`  
		Last Modified: Tue, 04 Nov 2025 23:26:44 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5314ea0df508fb596b80989a823b3f53e6f99e021b6e51ffb7e45a153bb87fb`  
		Last Modified: Wed, 05 Nov 2025 01:16:20 GMT  
		Size: 135.5 MB (135521735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57a00185430f912e160cd8f204d4996a1a93caf3ee276efdd4537715d78dbe6`  
		Last Modified: Tue, 04 Nov 2025 23:26:44 GMT  
		Size: 59.5 KB (59523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a506f3c865f4bd6ebb0c48b6578820939052cf4886cf18ac72fe2f09500a48f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11336573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc06cec166a17070be85399bb23ce894455a44072107bc0d451320281db5862e`

```dockerfile
```

-	Layers:
	-	`sha256:c67a45fe99bf3eda722a45f10d4c74499da008c872ea010cfb2f38fa557da0f3`  
		Last Modified: Wed, 05 Nov 2025 00:22:21 GMT  
		Size: 11.3 MB (11314774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33c90bef227c4fc85d0d855047f68a68d10e79103154077e817deebbf4c85759`  
		Last Modified: Wed, 05 Nov 2025 00:22:22 GMT  
		Size: 21.8 KB (21799 bytes)  
		MIME: application/vnd.in-toto+json
