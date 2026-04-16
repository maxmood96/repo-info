## `gradle:jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:64d7f0887b411fb2165eee8b650a2acc2c9b37d78e33893d49a061ab92f5b42a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:7eaeb7dfc46dc1119bf96ab66f52f458b74a76db4d7af5df8075264ef44b70f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **588.4 MB (588395086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa995c7dfd17b018a6c58d6c1d3d5e566b4916a99c0f695489f31b1e45eaaf93`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:24:08 GMT
ARG version=1.8.0_482.b08-1
# Wed, 15 Apr 2026 21:24:08 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:24:08 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:24:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 15 Apr 2026 22:18:22 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:18:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:18:22 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:18:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 22:18:22 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:18:22 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:18:22 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 15 Apr 2026 22:18:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 15 Apr 2026 22:18:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:18:25 GMT
USER gradle
# Wed, 15 Apr 2026 22:18:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 22:18:25 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d865abc8958d904089134e6afbdd634333b4eafd515c4ac99168fa07172cc37`  
		Last Modified: Wed, 15 Apr 2026 21:25:04 GMT  
		Size: 330.9 MB (330924355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ac7d71afc0f8eacfd88b1d6c0977cc04f3b89abe019bd791c4980714cd5deb`  
		Last Modified: Wed, 15 Apr 2026 22:19:11 GMT  
		Size: 65.5 MB (65454309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04665f9696bedd8822fcedd6970be29c2a67f03350ca181a86c83c00c202c699`  
		Last Modified: Wed, 15 Apr 2026 22:19:06 GMT  
		Size: 1.9 KB (1942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818edb2d1af1e4c13732188b476b103a2ed7afbf833e82fa4065fee81068849b`  
		Last Modified: Wed, 15 Apr 2026 22:19:12 GMT  
		Size: 137.4 MB (137388300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2f13fd420c2f7e96f03544b07b20d23d39611ba0b7c0528686b9b95081a8c3`  
		Last Modified: Wed, 15 Apr 2026 22:19:06 GMT  
		Size: 54.9 KB (54894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:05b0ae2c5787e125bb5ea0d22b546f2d0f0c439c9ac2d09b83fb2f215febdf1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18183563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b31e9de45eb8ce15ba25309c73fed81c3123b4df5bdda06a2985cbb885ae8128`

```dockerfile
```

-	Layers:
	-	`sha256:efdbd6a1f1493be3508f8f6f9a2b93e83b3a9e7b4d204801f09883b6147f5245`  
		Last Modified: Wed, 15 Apr 2026 22:19:08 GMT  
		Size: 18.2 MB (18162047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd7225077624c4cd1782e3f409d569d5dd726600c24194d41aa0fc2079efc53`  
		Last Modified: Wed, 15 Apr 2026 22:19:06 GMT  
		Size: 21.5 KB (21516 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:227c26d2e71f22536fd82e9f1511e36691cbfc217391d462a28025cfda30a668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.4 MB (394437310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:367ea1f01f673217c80820f69dddbf235a4c859e4a5ec57ddd7531110fc79c55`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:38:18 GMT
ARG version=1.8.0_482.b08-1
# Wed, 15 Apr 2026 21:38:18 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:38:18 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:38:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 15 Apr 2026 22:30:25 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:30:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:30:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:30:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 22:30:26 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:30:26 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:30:26 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 15 Apr 2026 22:30:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 15 Apr 2026 22:30:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:30:28 GMT
USER gradle
# Wed, 15 Apr 2026 22:30:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 22:30:29 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f5d61b99295ea1fb2b1e68202646ef07a17e94b3434367d80f0334607aa4c4`  
		Last Modified: Wed, 15 Apr 2026 21:38:39 GMT  
		Size: 118.0 MB (117961731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833430292f96f2d088c55053bf7b332ca3e674bc3de03ef0faf58ffa8025f21b`  
		Last Modified: Wed, 15 Apr 2026 22:31:07 GMT  
		Size: 85.6 MB (85583359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6c7e44afa1e17ec6f84e193e5fcb6187290e8a614ba07e8d86a664546480ce`  
		Last Modified: Wed, 15 Apr 2026 22:31:02 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28d489b2720fe4aac2365a732c525a6cc8e0d20877a9520bcce65174900f5c4`  
		Last Modified: Wed, 15 Apr 2026 22:31:08 GMT  
		Size: 137.4 MB (137388269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da90f0ef5015c120403706fdf5efc7007fa02d0a68fb2bd644ac7a3ac2be33e2`  
		Last Modified: Wed, 15 Apr 2026 22:31:02 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:37998c8613f16ebaa029a3053cfdcb7e9eb6a7c833e54531c772aaace2e88f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11747948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1c487e17b7ba1f6eaed9299c66ec618ef2d38f598a656db7920a990a523663`

```dockerfile
```

-	Layers:
	-	`sha256:e14a381e8c95492b67ca35a5cd57774dbb5833d1584f9bb8828dbbdffa8f996d`  
		Last Modified: Wed, 15 Apr 2026 22:31:03 GMT  
		Size: 11.7 MB (11726235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1943b1e6d793599268a0972b702ae4601d9cb18b019c90d4a10561c24288a65`  
		Last Modified: Wed, 15 Apr 2026 22:31:02 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json
