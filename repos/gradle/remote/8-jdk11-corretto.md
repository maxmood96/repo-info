## `gradle:8-jdk11-corretto`

```console
$ docker pull gradle@sha256:93d9f84a044faf9b345b7c126772ba719195318b0e848e322c6f1a977232e012
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:4bf09654bcef30b8fa97d540bfbb8bbed69a974f52f5aabb8d73b909313c0a1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430881441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36afc6c33138c594aecb81c8c30e745961fd337ba774b9993fee20aefe025c3c`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:57 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 18:59:57 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:57 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 21 Jan 2026 19:17:14 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:17:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:17:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:17:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:17:14 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:17:14 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:17:14 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 21 Jan 2026 19:17:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 21 Jan 2026 19:17:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:17:16 GMT
USER gradle
# Wed, 21 Jan 2026 19:17:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 21 Jan 2026 19:17:17 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a07ea5032c792d7ba679b74d72cf278e3e104563477a78ec86bb42a7f99648e`  
		Last Modified: Wed, 21 Jan 2026 19:00:16 GMT  
		Size: 153.4 MB (153367384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56f3c4ddd98e4a3de0705a42364c043939702414a62bf0f359ade0b38f83dd7`  
		Last Modified: Wed, 21 Jan 2026 19:17:48 GMT  
		Size: 86.0 MB (86041071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:118a4b1ee5f740dd555248b1abafb3e035669146b379b100f774d2f6027c4994`  
		Last Modified: Wed, 21 Jan 2026 19:17:45 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d720e3ce55899e78143ac487504f3645d2c6be76b28bad4e7ddcc8fd2ceb5e0`  
		Last Modified: Wed, 21 Jan 2026 19:17:53 GMT  
		Size: 137.4 MB (137395197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2f054da4db37d43c643ccadd3cd8dc58362591269fa61985230d2c23ed06e6`  
		Last Modified: Wed, 21 Jan 2026 19:17:45 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:41a262d6aa8465b4e44605b322dcf2fdfe3ec86e31c195ecc2bb703906b3040c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a47d323a47a82f496b61226ad292f1177dea08e1c8ff590341f69ac6741cb4b`

```dockerfile
```

-	Layers:
	-	`sha256:1f735f0d57eb34e437f00bcf960ff289d8b1ab9a608c81593aa3e3d0b526aa01`  
		Last Modified: Wed, 21 Jan 2026 19:17:45 GMT  
		Size: 11.4 MB (11366000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1672ee9d2f8695900282b157b8a4d0a34feade2fc192003227a745a1f7a2643e`  
		Last Modified: Wed, 21 Jan 2026 19:17:45 GMT  
		Size: 21.5 KB (21523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:cdeb5ba97db024921361e4975424e85853a117056b9bb599a322052d16ed4b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.8 MB (427813445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7692f7c15ded2c8607e63ddcd03d6443a04d67427a9a18a8c8e6d500ef5302f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:16 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 19:00:16 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:00:16 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 21 Jan 2026 19:17:11 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:17:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:17:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:17:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:17:11 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:17:11 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:17:11 GMT
ENV GRADLE_VERSION=8.14.3
# Wed, 21 Jan 2026 19:17:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Wed, 21 Jan 2026 19:17:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:17:14 GMT
USER gradle
# Wed, 21 Jan 2026 19:17:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 21 Jan 2026 19:17:14 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436dca49d48a119ba29e5c58e3826eb3069953cb00876a3cfc8081de1fdd358b`  
		Last Modified: Wed, 21 Jan 2026 19:00:39 GMT  
		Size: 151.9 MB (151921187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4102417eb2813b9c6b1eb83f369d800031e59a67b44411d1a8d692106c90f169`  
		Last Modified: Wed, 21 Jan 2026 19:17:46 GMT  
		Size: 85.5 MB (85521494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9291745786e80785f2857f545abb40506562f88cfd05a49fce527e57b7d87598`  
		Last Modified: Wed, 21 Jan 2026 19:17:42 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d57249acb4ab7433f8e1453df8e33d9a3432483b897e4062a65419bc4451ad`  
		Last Modified: Wed, 21 Jan 2026 19:17:47 GMT  
		Size: 137.4 MB (137395201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a55ae70bf231ee557ff095da6e8b73acd4e59031e6dafea72c7512db69bbf`  
		Last Modified: Wed, 21 Jan 2026 19:17:43 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:f1cb768e2767c78c78c9153528acf4194692fe87550c552f0a40f2be8b89c2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9819d8646810ec1bda8f95f2161b33884ac54846ab03aab66299ee40ba715a8`

```dockerfile
```

-	Layers:
	-	`sha256:87fea1b1ff343ecac8729018698ff5dbb83551985e55c8620e04487a05e010e4`  
		Last Modified: Wed, 21 Jan 2026 19:17:43 GMT  
		Size: 11.4 MB (11365843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23bc015531c9fd2cc4f4004e1858f6b6142a7ea0d43141837c0d3f3edbb909cc`  
		Last Modified: Wed, 21 Jan 2026 19:17:42 GMT  
		Size: 21.7 KB (21719 bytes)  
		MIME: application/vnd.in-toto+json
