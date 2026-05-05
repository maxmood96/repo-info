## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:47bfcd2a74ed12c978918b0d7dbd2e229c7ce2708cbf26285cc0bdb952e3692a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:dd1b1d3b1d0844147170c3625137e763da83293ebbbe7ad0f09ba0050b7a672b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.4 MB (579422487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d309037930c4a4c6ecff84581896544c74aca6219125797e91e1f5a1631bfa1`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:42 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:11:42 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:42 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 04 May 2026 20:42:57 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:57 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:57 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:57 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:57 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:57 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 04 May 2026 20:42:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 04 May 2026 20:43:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:43:00 GMT
USER gradle
# Mon, 04 May 2026 20:43:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:43:00 GMT
USER root
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd2ff23a0524b1c7113ef94f2af3cff82ef1d7e86189b3e37a0a49a3e8a4e2c`  
		Last Modified: Mon, 04 May 2026 20:12:39 GMT  
		Size: 330.8 MB (330812379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9d5725f33db30bef5cec1766a8adabc1e260067fa3fbcc8d2d61b46f3a88bd`  
		Last Modified: Mon, 04 May 2026 20:43:42 GMT  
		Size: 65.5 MB (65507039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4007e42e3e4ae6bcca89f8e7fbcb5bbbcae6b8c3cf0c2379ae75711a191555`  
		Last Modified: Mon, 04 May 2026 20:43:38 GMT  
		Size: 1.9 KB (1944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0923307b779844d15b59363b5f7665b0f5a9d05def963567b7aa031fa93f4dfd`  
		Last Modified: Mon, 04 May 2026 20:43:43 GMT  
		Size: 128.5 MB (128469438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2f685baa03bc5fb578859be3b82862cd7c396086c3087e086aaebf9477e26b`  
		Last Modified: Mon, 04 May 2026 20:43:38 GMT  
		Size: 54.9 KB (54902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:391078f83f326558a7ecb6dae626af023e05a92da26774c1d260745c0a0413c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18094408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecf89a8c0e136ed435e36c163eb2ce24179a03ee81ef708b1edcc636d8763f1`

```dockerfile
```

-	Layers:
	-	`sha256:2c957cbac9a6446eda977c8553e1abbaddc3f17cf6b3bd908024c0e22133b622`  
		Last Modified: Mon, 04 May 2026 20:43:39 GMT  
		Size: 18.1 MB (18073545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992256094b3dc5b4092a6aa7b013b78175d27c9d8c6c33f43f7dd12310f2f85d`  
		Last Modified: Mon, 04 May 2026 20:43:39 GMT  
		Size: 20.9 KB (20863 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:b5996f859c5a5aa8c8f2c92a02de02f31876864802b9d272412fb271d5253ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.6 MB (385589940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6ebd304b4cacbdc54e2823193877b821948588102a8740b79b433a01affd9b`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:02 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:11:02 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:02 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 04 May 2026 20:42:49 GMT
CMD ["gradle"]
# Mon, 04 May 2026 20:42:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 04 May 2026 20:42:49 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 04 May 2026 20:42:49 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 04 May 2026 20:42:49 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 04 May 2026 20:42:49 GMT
WORKDIR /home/gradle
# Mon, 04 May 2026 20:42:49 GMT
ENV GRADLE_VERSION=7.6.6
# Mon, 04 May 2026 20:42:49 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Mon, 04 May 2026 20:42:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 04 May 2026 20:42:52 GMT
USER gradle
# Mon, 04 May 2026 20:42:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 04 May 2026 20:42:52 GMT
USER root
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f663ff8f95b0ac33e5eeb3a57969767ad4ebbcf9ffbf6f56257306287e40928`  
		Last Modified: Mon, 04 May 2026 20:11:22 GMT  
		Size: 118.0 MB (117962667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cd931a7a9f247850ab74b50b828e0d3612210ab308faf81cd35e9fdf3bc41b`  
		Last Modified: Mon, 04 May 2026 20:43:23 GMT  
		Size: 85.6 MB (85639880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a70c7b588bd96f048ac1e2f49f878a7e3cfdd7d19f16af31a9a7b8b712216fb`  
		Last Modified: Mon, 04 May 2026 20:43:19 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbef5c665ae27a3afab19981cd8a48d1dcb9b790beec9bb551e6a2ec69e27193`  
		Last Modified: Mon, 04 May 2026 20:43:26 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cf72138b67680469c72decd7ba46a50f30c15a9089ce5becaa2ef48a44af8b`  
		Last Modified: Mon, 04 May 2026 20:43:19 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:be1ea8d13e18ebf0d645d4ac5a4d081f65689a52eda9cab7fe749f7459ef355f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11658750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efa5572834db42216d2e2e2b4cbe6037453ceca5654c0acbb2ad01f8769b068`

```dockerfile
```

-	Layers:
	-	`sha256:94fed7ae08abe6ba2a46c4d85ad7138a0dc299af09e02fb118177757d89a9976`  
		Last Modified: Mon, 04 May 2026 20:43:20 GMT  
		Size: 11.6 MB (11637713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628f3c75997e64be81b66c0edb79d56521183a5fac9f321d9618df6e3cd8094a`  
		Last Modified: Mon, 04 May 2026 20:43:19 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json
