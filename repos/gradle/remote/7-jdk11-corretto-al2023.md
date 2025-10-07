## `gradle:7-jdk11-corretto-al2023`

```console
$ docker pull gradle@sha256:d25cf95d157c8f7dd019a47f86d28470488fa374a5e0288622be11cc32f28ed5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk11-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:a24d8216a0b61331c61014e3f03ee2780dfdb03551d82596fdcbff9f67536a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.2 MB (422164817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d766958e03642f27e19b62ce65f2955d8c9857815a2f5e387c8531c137d20635`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 23 Sep 2025 15:37:00 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:37:00 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 23 Sep 2025 15:37:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER gradle
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER root
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bea491ccf4f1cb4479c0d0dd695e9eaea15d1c73558a4e304bd3314fb876293`  
		Last Modified: Mon, 06 Oct 2025 22:11:15 GMT  
		Size: 154.1 MB (154072396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205dda72b57e8c869696f5ecb8c06e423f2e15e8044065a0d338b3dbc782910c`  
		Last Modified: Mon, 06 Oct 2025 22:13:28 GMT  
		Size: 85.6 MB (85561288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b687b68edf217ce61a1cd0fba7033302350a85dbbbac63d472f2fc117bf0a0`  
		Last Modified: Mon, 06 Oct 2025 22:13:01 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad99fbb419124bd1117f3e62607b841628a01f736a7712bae55e22daf2f16b9`  
		Last Modified: Tue, 07 Oct 2025 13:49:21 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cb1fec23416c5f6927eb8837daf25624f95c30c75d805c30edc00244b270b9`  
		Last Modified: Mon, 06 Oct 2025 22:13:01 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:7e687b15e658da12a5d27464fc7677f2b9bd88d2fd347239bf025d09493eda88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11268542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9978173a3c6a5d8a4ee83504f7b231909f70f773501ec67b6749f0d3ab72d98`

```dockerfile
```

-	Layers:
	-	`sha256:17942308c9cfa0f51d23ee0e82c05bb6b94daefbf018a650d7aa2998bbb77484`  
		Last Modified: Mon, 06 Oct 2025 23:18:40 GMT  
		Size: 11.2 MB (11247628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca19e0b9bdda16e290d3d002747c8361fdb867534036aa5eab30c69f2f5d2e92`  
		Last Modified: Mon, 06 Oct 2025 23:18:41 GMT  
		Size: 20.9 KB (20914 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk11-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f7f077e6104184b7ed7dd328648e132ace7c1d640574ee4f9239a8e0f785989b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.1 MB (419089124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb421d25c308221371c83eea6d14011ec84a68b3562d918de4e8d8da1762722c`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 23 Sep 2025 15:37:00 GMT
CMD ["gradle"]
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 23 Sep 2025 15:37:00 GMT
WORKDIR /home/gradle
# Tue, 23 Sep 2025 15:37:00 GMT
ENV GRADLE_VERSION=7.6.6
# Tue, 23 Sep 2025 15:37:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER gradle
# Tue, 23 Sep 2025 15:37:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 23 Sep 2025 15:37:00 GMT
USER root
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60693563db8a15ef6cbbb254b5f7cdd25c3f0b7dea83ba28e605d00261462016`  
		Last Modified: Mon, 06 Oct 2025 22:11:35 GMT  
		Size: 152.6 MB (152580439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fe036e7dff3ade3efe77678a774cf65ec0db43e2c587cc9cb9141494c05408`  
		Last Modified: Mon, 06 Oct 2025 22:13:08 GMT  
		Size: 85.1 MB (85086862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acedcd67ff50367f1c39f074be00b1acf3baa0d8f741b3bdcdff2fc4852a7121`  
		Last Modified: Mon, 06 Oct 2025 22:13:03 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45237b6cffe76e492f2aa8f3bb8f008e1bb29a639ef0c3d7a06fb561c891ca58`  
		Last Modified: Tue, 07 Oct 2025 07:46:44 GMT  
		Size: 128.5 MB (128469413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee5726ad77c70c68de0603e32702ac11fac1c4194448bf032f08a6e95280f26`  
		Last Modified: Mon, 06 Oct 2025 22:13:02 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk11-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:02b54039c0a6eefaafd5ccf937fd4d616ea06cb722005947042e65f0510e9e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11268530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6730c2d8f8020c856e6e699cce5fe04c06eea62e9faf9f18d069e8f6916456`

```dockerfile
```

-	Layers:
	-	`sha256:65dfa567261f5f0ce472977404e6b14fad5f0b82fee408f18bc3c242d54b6377`  
		Last Modified: Mon, 06 Oct 2025 23:18:50 GMT  
		Size: 11.2 MB (11247443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ed6467afb73aa1a794fa330bfc1aaa06247caa483d5bb19039b270ae5fa353a`  
		Last Modified: Mon, 06 Oct 2025 23:18:51 GMT  
		Size: 21.1 KB (21087 bytes)  
		MIME: application/vnd.in-toto+json
