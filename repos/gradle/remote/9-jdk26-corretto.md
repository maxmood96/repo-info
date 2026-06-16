## `gradle:9-jdk26-corretto`

```console
$ docker pull gradle@sha256:5ba11eab80663869104392bc18b66e21b7f7f6cc40389c521f974675a3a8787b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk26-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:0981520a106e1388c81a91e57ec414150771e84709d0fc39606ff440c86b38ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.6 MB (474550439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd8185c4d551ec18f91b89a784e01b8b0eb3eb5e7829e0e9c939684821763bc`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:27 GMT
ARG version=26.0.1.8-1
# Tue, 16 Jun 2026 01:16:27 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:16:27 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:16:27 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Tue, 16 Jun 2026 02:19:37 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 02:19:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 02:19:37 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 16 Jun 2026 02:19:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 02:19:37 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 02:19:37 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 02:19:37 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 16 Jun 2026 02:19:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 16 Jun 2026 02:19:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 02:19:40 GMT
USER gradle
# Tue, 16 Jun 2026 02:19:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 02:19:41 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6c92ee6070c4cf419dd8cb75768f6678ec4db82914dc600f4679f29e3e6feb`  
		Last Modified: Tue, 16 Jun 2026 01:16:51 GMT  
		Size: 193.4 MB (193448363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a01bbbab2b986aa9db0c9f5351945061c27e8334392734386572fa3ddea844`  
		Last Modified: Tue, 16 Jun 2026 02:20:12 GMT  
		Size: 86.3 MB (86266626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8079f455ac531d7a506ab44b2c138858d75c4f1741c6c0e059a6bbea7c998c`  
		Last Modified: Tue, 16 Jun 2026 02:20:08 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9790d1f6fccfabecfd5b1eb8673067024ae1f34973415300255c9d659890902a`  
		Last Modified: Tue, 16 Jun 2026 02:20:13 GMT  
		Size: 140.2 MB (140236983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25018f735febe809603155a3432b5549dbdf25ad28d786d5ad45169e6286dde`  
		Last Modified: Tue, 16 Jun 2026 02:20:09 GMT  
		Size: 25.6 KB (25630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:39ff132a2045847b333796e8c9c4e2c135205bc747302acd1ae5c06665a30944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f961ccc5a4193913f4880a331e669359dc0289e94de76d14ad5e25f0a9fd9aed`

```dockerfile
```

-	Layers:
	-	`sha256:c25a928c506c318c3004da87dba27a16983a19dab7d8e059de516893416f6cc7`  
		Last Modified: Tue, 16 Jun 2026 02:20:09 GMT  
		Size: 11.4 MB (11375548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8675d9f445108d62ddb6b76d95a83bd31ea7c457caf6a22b437de05215a70c03`  
		Last Modified: Tue, 16 Jun 2026 02:20:08 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk26-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a6fdb7e39f5ce7b1788591bfa4d82f3ef9248ae00f3ce572562f67acbd559090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.7 MB (470719521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ca177ff6f668f7182f13001e74ab21e7d09bd5f8e30414933dbee2e47058fd`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:17:32 GMT
ARG version=26.0.1.8-1
# Tue, 16 Jun 2026 01:17:32 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:17:32 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:17:32 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:17:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Tue, 16 Jun 2026 02:20:20 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 02:20:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 02:20:20 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 16 Jun 2026 02:20:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 02:20:20 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 02:20:20 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 02:20:20 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 16 Jun 2026 02:20:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 16 Jun 2026 02:20:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 02:20:23 GMT
USER gradle
# Tue, 16 Jun 2026 02:20:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 02:20:23 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492d28854898d07428811a019380c62492f7040cc40abee715bfd95faac1e00b`  
		Last Modified: Tue, 16 Jun 2026 01:17:58 GMT  
		Size: 191.3 MB (191270312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13234ac739782b15c83e2e17b05b6b3843331804934edcfb367e821768e85863`  
		Last Modified: Tue, 16 Jun 2026 02:20:55 GMT  
		Size: 85.7 MB (85723383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb6a4167c7ae5649a20ad13d8287313fcefe29577453503453b930f67c2e9c`  
		Last Modified: Tue, 16 Jun 2026 02:20:51 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630f352a6d70af2a90f687cb703a19795a5cc1443afad973d90cb66034fd2c77`  
		Last Modified: Tue, 16 Jun 2026 02:20:56 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfe12bbfa141c1b204e272b8edd0e802b2aa1c90843e89d3bc7ebc4bfc07e6e`  
		Last Modified: Tue, 16 Jun 2026 02:20:51 GMT  
		Size: 29.3 KB (29336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk26-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:0716207fa1ed3944eac1183aa30944d782092e40206f0c6a05465d3ac076cd91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11396405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d91731fc8aabec2ea890394411c1c9c22dc7ea692673690acfb3ddbce1b074`

```dockerfile
```

-	Layers:
	-	`sha256:522e526877e406088f5321061890dadd58f1aa078021531d9df6bd5d4699ad5b`  
		Last Modified: Tue, 16 Jun 2026 02:20:52 GMT  
		Size: 11.4 MB (11374557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7131e5677ce5ffdadb973862f1e575fbb6d3a296d012a951a1510801ae9d3a7`  
		Last Modified: Tue, 16 Jun 2026 02:20:51 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
