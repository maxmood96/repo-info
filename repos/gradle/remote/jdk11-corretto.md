## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:a32d0624df3fb5ddc15bed987a677c2d02c8cede64337ab74c5e24763dc21708
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:03e27bbc39ecd86a8b8e2fe07494c3ce212ffcab9cc1cfb13df1864c381f1739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.4 MB (417448135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e420c149343cf5ca62fd09e4bfc410350713135c3287d936bffa34e4dec15c8`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=11.0.26.4-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 27 Mar 2025 21:20:39 GMT
CMD ["gradle"]
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 27 Mar 2025 21:20:39 GMT
WORKDIR /home/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_VERSION=8.13
# Thu, 27 Mar 2025 21:20:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER gradle
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER root
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8881ccee6b0b939818e89f9577da887036a6c3064496209af2d60c6727cbde4b`  
		Last Modified: Tue, 01 Apr 2025 23:59:14 GMT  
		Size: 154.0 MB (153989030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54a5839039d4bd2793aecac608d0de7c5321b6c41e78c8c27f99ec456d9660`  
		Last Modified: Wed, 02 Apr 2025 00:08:21 GMT  
		Size: 70.5 MB (70507294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6764f53fa4e20febbd1ebe0c33711df3fad28143ea4be5602f9dc23e706c7361`  
		Last Modified: Wed, 02 Apr 2025 00:08:20 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13b9474b74229739d4bdb824e97e44b682cd2d5ec14c356865e809bbc049c26`  
		Last Modified: Wed, 02 Apr 2025 00:08:22 GMT  
		Size: 137.0 MB (136988177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232bb103afba3dbab04ab4c4134ffc551ae7bf3b1beeab8b13164cdcdd755b8c`  
		Last Modified: Wed, 02 Apr 2025 00:08:20 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7e3790110485dbfc17bb75af4646445ed6408f63ce0b6c059d32a9d7b6ada577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10792211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08c328adec8974eef910bcbce3f29581b6d92eab03c0eb8d9e85faec51467c79`

```dockerfile
```

-	Layers:
	-	`sha256:d90b8cfe4a7ef1fe771061f8567c6fe6838a8931878edeeb03b02efd2b35d516`  
		Last Modified: Wed, 02 Apr 2025 00:08:20 GMT  
		Size: 10.8 MB (10772311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67560f361d4c36ff099c1cb9083811f9d27851ba3c715702b2e6eae164e5b11`  
		Last Modified: Wed, 02 Apr 2025 00:08:20 GMT  
		Size: 19.9 KB (19900 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:93f122698200ea6ef503e216b54b6e3dc5b55fa93ec7132ef7e71e6268102293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.5 MB (414462759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26451002c81351b315e9f458a120a9e31f5346f7154421451e9d48e163349122`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=11.0.26.4-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 27 Mar 2025 21:20:39 GMT
CMD ["gradle"]
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 27 Mar 2025 21:20:39 GMT
WORKDIR /home/gradle
# Thu, 27 Mar 2025 21:20:39 GMT
ENV GRADLE_VERSION=8.13
# Thu, 27 Mar 2025 21:20:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER gradle
# Thu, 27 Mar 2025 21:20:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=20f1b1176237254a6fc204d8434196fa11a4cfb387567519c61556e8710aed78
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 27 Mar 2025 21:20:39 GMT
USER root
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0aa06b2e36ca9878b02b7767aa08a65ff17b8f983836cce29b24cc0963764c`  
		Last Modified: Wed, 02 Apr 2025 00:28:37 GMT  
		Size: 152.5 MB (152478575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f983e76443c373b7ca6c86ec2777232b4564bf43224dc9deb29531c8caade516`  
		Last Modified: Wed, 02 Apr 2025 01:10:23 GMT  
		Size: 70.0 MB (69973789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad07bf17650ed54a0ea7dc0c55b22f56a9526d665eff587c5b735c55287bdec`  
		Last Modified: Wed, 02 Apr 2025 01:10:20 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89199cc55516584d062ebe1a42f41b1bc390f2e71a7c7b2e732bb51ee6ef5583`  
		Last Modified: Wed, 02 Apr 2025 01:10:25 GMT  
		Size: 137.0 MB (136988176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37bd3b2bc5d444dd8dd1473cf879bf74f62f2b4b89b1da87dfcb7675853a21a`  
		Last Modified: Wed, 02 Apr 2025 01:10:21 GMT  
		Size: 59.5 KB (59535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b303c57c778c9f9a5e0aa6ede19efa2e2db7644e4d3719e204fe38b4dddcc6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10792251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea5136440a6dad2e1ae325a0b56527a7b8109dafe354d3bcbe6983896c1c0d4`

```dockerfile
```

-	Layers:
	-	`sha256:22f922c0d6d5460627ce8c3bc18e09d7c479a4b08f6daff13dd27579ec46842f`  
		Last Modified: Wed, 02 Apr 2025 01:10:21 GMT  
		Size: 10.8 MB (10772154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8db0a261449851b6b250046b93d63adf64c6491bb1b2cea09ea18b50e2e6e31`  
		Last Modified: Wed, 02 Apr 2025 01:10:20 GMT  
		Size: 20.1 KB (20097 bytes)  
		MIME: application/vnd.in-toto+json
