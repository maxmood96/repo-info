## `gradle:7-jdk17-corretto`

```console
$ docker pull gradle@sha256:421c62b09d2b287a2c2f445a4421eefcaec36a3345df4a261822a9bb3702c266
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:50b9863460a5a2279e052062bae1b08098f9faed65aaf5574b811d42c1efd005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.4 MB (426423674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8240295b6d92f45b5d34ac6bb0192aff88d732ca9f89eff0f7569fd9fe153298`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:21 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:12:21 GMT
ARG package_version=1
# Mon, 04 May 2026 20:12:21 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:12:21 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 04 May 2026 20:42:25 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:25 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:25 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:25 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:25 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 04 May 2026 20:42:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 04 May 2026 20:42:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:28 GMT
USER gradle
# Mon, 04 May 2026 20:42:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:28 GMT
USER root
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be73c3ad3366393074a6eed7a125da1ff3733ec46325d456499b501d1e3f64ea`  
		Last Modified: Mon, 04 May 2026 20:12:44 GMT  
		Size: 157.2 MB (157155466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c044030b1e444e9fb14434728b01d5f50127289e4ad57a51f212a27b6686b2d9`  
		Last Modified: Mon, 04 May 2026 20:42:57 GMT  
		Size: 86.2 MB (86165461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed0afd1a1947219375a44e9d6ba83d8f1b76d9ceb2be82b5107aa5176aaab66`  
		Last Modified: Mon, 04 May 2026 20:42:53 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910a6365ed95723d1b370446e7c5ed946b970c883ad68937d272ecb3c9c05236`  
		Last Modified: Mon, 04 May 2026 20:42:58 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85794580b8c73c5ecad1b2aaf4c178cc0784fe04c4b82217dcab06524cdaf316`  
		Last Modified: Mon, 04 May 2026 20:42:53 GMT  
		Size: 54.9 KB (54897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:8c84e820389605362db9202a8854aa594924364df705700f635b7a984353d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11281700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fa9316633eb776df1f8e7e6d3c83bf846cd3044c38152df1d1d3f9e345bbe8`

```dockerfile
```

-	Layers:
	-	`sha256:e47eb150a3f55bb90610bbaeebafb0972158f45061666dff55a6ee909b23edb7`  
		Last Modified: Mon, 04 May 2026 20:42:53 GMT  
		Size: 11.3 MB (11260987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7162454a9d723bd878d23d09a38e803a189712e21bf070c44367caf37b66dc9f`  
		Last Modified: Mon, 04 May 2026 20:42:53 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:bbe3d77e1a1d1084f66b4f27ef199a2230887733af618acb5cb109d379ef9d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.6 MB (423630979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ebd62fb02bad5f436fccbb29cd5c7a06375b27d6f984c1d593ec8bd0a02ad0`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:40 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:11:40 GMT
ARG package_version=1
# Mon, 04 May 2026 20:11:40 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:40 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 04 May 2026 20:42:24 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:24 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:24 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:24 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:24 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:24 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:24 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 04 May 2026 20:42:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 04 May 2026 20:42:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:27 GMT
USER gradle
# Mon, 04 May 2026 20:42:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:28 GMT
USER root
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322640e3642311a443627a18ff0c4fa0690feddc7c348c64a06d1c5fdac713ba`  
		Last Modified: Mon, 04 May 2026 20:12:03 GMT  
		Size: 156.0 MB (155989760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:227bf7dd8e5373189e14fbfe4f69e018f601004f49a99b2d82541cb3a6539763`  
		Last Modified: Mon, 04 May 2026 20:42:59 GMT  
		Size: 85.7 MB (85653823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839cda8b44f5b0f5760a01be88498616bf8a5d9b617af09228e5576747b8410d`  
		Last Modified: Mon, 04 May 2026 20:42:55 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4a500f59a1f5250d9d2a87a2421e46fe5df68f645369266bad0582ef354c458`  
		Last Modified: Mon, 04 May 2026 20:43:00 GMT  
		Size: 128.5 MB (128469419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219d385c58dc7317b24e318d7fb66f0e063e7cb1055496fbaea5585df47567ac`  
		Last Modified: Mon, 04 May 2026 20:42:55 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:89052e1fccdabfd011a59c0a8c00108a630a1f1627a56ac672ee17f4c080a50a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11280845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ece438c50c4cd4764e171dfddf89089629fab7e01556583c5a3aad734f0faee`

```dockerfile
```

-	Layers:
	-	`sha256:5366981204058a28be27b01d0ae080331c25b3a003246408f19c278e238dc139`  
		Last Modified: Mon, 04 May 2026 20:42:56 GMT  
		Size: 11.3 MB (11259959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4642e533c3355484064439d70f4a4fb19e33c5868563f7c1cd95479e2559319`  
		Last Modified: Mon, 04 May 2026 20:42:55 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
