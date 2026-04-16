## `gradle:7-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:d15fe170b53f90e722c2e95ef99e86a913dc9eb696a63de6d681744b93085abf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:883d92a099045fcd22070d93c9d9f5cf1fa9b83ddc58f216fbf9382dd1789026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.1 MB (426109868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b840485a9c7b2722ea3f39385081b73f99527480059ce3b3802c8483f31a60fe`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:07 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:26:07 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:07 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:07 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 15 Apr 2026 22:18:08 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:18:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:18:08 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:18:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 22:18:09 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:18:09 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:18:09 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 15 Apr 2026 22:18:09 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 15 Apr 2026 22:18:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:18:11 GMT
USER gradle
# Wed, 15 Apr 2026 22:18:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 22:18:11 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008cbcc9cf06909dadd7713e6243b1a02925fac6d3632b00ee5b3c83554fe53c`  
		Last Modified: Wed, 15 Apr 2026 21:26:29 GMT  
		Size: 156.9 MB (156911119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e521d4f1ae2448fe33728675b40c7216bc84a936a4cba345ad29c05eb4b47f4`  
		Last Modified: Wed, 15 Apr 2026 22:18:41 GMT  
		Size: 86.1 MB (86101483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:badd28ea94820c862103c74a6a3672215425e1be356fcdb824f05238c0a70842`  
		Last Modified: Wed, 15 Apr 2026 22:18:37 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a11544de7d2b01f54cfcbe23895c4775a1daa23213314d83f10c859a663554c`  
		Last Modified: Wed, 15 Apr 2026 22:18:42 GMT  
		Size: 128.5 MB (128469440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cc6135f7065bfaed90fdb5987dbd01127a1236d98a5b576acfa7f0e2846cfe`  
		Last Modified: Wed, 15 Apr 2026 22:18:37 GMT  
		Size: 54.9 KB (54890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:4e848374fa842a3a2e5fe38226b02d4be777b0e639d1ef23997a3b9e1b1cc740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11279370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b3f56434548b07d2279d597ebdae18fae3143f1168b6689b675d3f236fcd43`

```dockerfile
```

-	Layers:
	-	`sha256:2ce969e1161220c271d631c9b3ca061fcacaef06b7e2d5b09b613825bdd022bc`  
		Last Modified: Wed, 15 Apr 2026 22:18:38 GMT  
		Size: 11.3 MB (11258657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7fd3d0d0a0ecd04d40160203aea81079b724b8dc4e81e7f6a25ae55cfea9ec`  
		Last Modified: Wed, 15 Apr 2026 22:18:37 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bd941c93cb9aaa8091c6b06a3032a4a7c7f7c335127f710b8ecf48a32c5747b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.3 MB (423305056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf3a28176ca22afcc8416b40bc5c3ad23933fb0b8878ee09a47cb6d46fb515f`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:06 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:39:06 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:06 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:06 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 15 Apr 2026 22:30:18 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:30:18 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:30:18 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:30:19 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 22:30:19 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:30:19 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:30:19 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 15 Apr 2026 22:30:19 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 15 Apr 2026 22:30:21 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:30:21 GMT
USER gradle
# Wed, 15 Apr 2026 22:30:22 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 22:30:22 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ece4200ddd22a4421c854fc02730d00179c130556075100cac3ac7322df40bb`  
		Last Modified: Wed, 15 Apr 2026 21:39:28 GMT  
		Size: 155.7 MB (155728403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1548385c11c128573e100493a4096538f561fdd63c7f2d03ad367d3129624924`  
		Last Modified: Wed, 15 Apr 2026 22:30:57 GMT  
		Size: 85.6 MB (85603293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86fe49ee98e329c5f41af79dfeb027a3ef4d686afff9b6b5ac8c71bbc55ed7c`  
		Last Modified: Wed, 15 Apr 2026 22:30:54 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0dfd7063201dc59246f8d5ce6ddd8da53013e4af85c15928445366ba75e501`  
		Last Modified: Wed, 15 Apr 2026 22:30:58 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c447327fffa1135cb37c5a9fe009e94073c979feb5c4d623043c1ef4be3f997`  
		Last Modified: Wed, 15 Apr 2026 22:30:54 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:23e1e4c6eebce7c3501eef53ecb67a3bc1520e5f4422be16ca11d6402a8e752e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11278514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff948d6a9a5bf40911565c9ae4e61b65a6eaf045a941579e1c915fe0be4ff9a3`

```dockerfile
```

-	Layers:
	-	`sha256:b0f4ceb8980de9d6e4b9403827e962c469fb8071c1a039695445da3fb275bdfc`  
		Last Modified: Wed, 15 Apr 2026 22:30:55 GMT  
		Size: 11.3 MB (11257628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6700673208abf6a25a671aa5228e8e75a8b726c9badc65ee80c25c8731276e6c`  
		Last Modified: Wed, 15 Apr 2026 22:30:54 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
