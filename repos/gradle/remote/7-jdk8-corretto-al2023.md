## `gradle:7-jdk8-corretto-al2023`

```console
$ docker pull gradle@sha256:da20892c717a73b35f72392fd2d1af8dd8624308aec243b3cc31a0d4e67e52b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk8-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:a4a8af2b64df7ac3ae7ed2b9bc2fa67ed6ed8f5ee8ba26b1ffccccd5cac8e8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **579.5 MB (579476290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29ae28622266d71a9c4d1c0806e77be42e429fd8d76615363822b3206890326`
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
# Wed, 15 Apr 2026 22:18:56 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:18:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:18:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:18:57 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 22:18:57 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:18:57 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:18:57 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 15 Apr 2026 22:18:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 15 Apr 2026 22:18:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:18:59 GMT
USER gradle
# Wed, 15 Apr 2026 22:18:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 22:18:59 GMT
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
	-	`sha256:aca55772f015b6d63eac12c74c7899f53b7b057a7265648a367e8bd38bcde55d`  
		Last Modified: Wed, 15 Apr 2026 22:19:39 GMT  
		Size: 65.5 MB (65454372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6d0fa3e14c5a832fc1f3e2737e9090f74261e19948cf00b1f238ba53eda2ba`  
		Last Modified: Wed, 15 Apr 2026 22:19:35 GMT  
		Size: 1.9 KB (1946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c33a4d600d99fc96e86d8b09287a928d50cedbed986bfd7e23d6df9e222d93`  
		Last Modified: Wed, 15 Apr 2026 22:19:40 GMT  
		Size: 128.5 MB (128469437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d889238a6503bb8138c3dcd9ec1547ddf358215cd8cf1dc9a5ae0b2c887ac169`  
		Last Modified: Wed, 15 Apr 2026 22:19:36 GMT  
		Size: 54.9 KB (54894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:5ea41784a5c2e458ddebb29ba8fae94a088fd0a85a6bbf4938aa158ec103a1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18092908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b71392d79a988b60b65167efc5713580a14f3ae24583db7681a6a605fa9948`

```dockerfile
```

-	Layers:
	-	`sha256:2cc75ee888dcc4aa3a9e1c8d372165663df13cc42b83acfdf57ec272c9bf912a`  
		Last Modified: Wed, 15 Apr 2026 22:19:37 GMT  
		Size: 18.1 MB (18072044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27963ee1a288354c935db6d4c9c573fa23bdfc014db892e977d077525909755a`  
		Last Modified: Wed, 15 Apr 2026 22:19:35 GMT  
		Size: 20.9 KB (20864 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk8-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:a0ccc686af713c1dddbc7d3faf65f0a26f780bcb0a358b4d55d870232438f069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 MB (385518969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f29e843c5012582ee154c8698bd89944b46d25db19c3a7c8734e257e7c7a0db1`
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
# Wed, 15 Apr 2026 22:30:54 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:30:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:30:54 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:30:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 22:30:54 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:30:54 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:30:54 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 15 Apr 2026 22:30:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 15 Apr 2026 22:30:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:30:57 GMT
USER gradle
# Wed, 15 Apr 2026 22:30:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 22:30:57 GMT
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
	-	`sha256:c1eb3610d8791e375652714ebedd654e4af56cb708a49ce620e30b0e1aa80a43`  
		Last Modified: Wed, 15 Apr 2026 22:31:29 GMT  
		Size: 85.6 MB (85583876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324e53670d052903c3225b82a7718c4b6fae3a1e898530033392993ba40c08fd`  
		Last Modified: Wed, 15 Apr 2026 22:31:25 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674d25fcfc78def07f3ad959859037fc99337a5dd74e0d18c97fe24f1ef08b06`  
		Last Modified: Wed, 15 Apr 2026 22:31:30 GMT  
		Size: 128.5 MB (128469421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054329f14d0f29f53c116ad3e596b99346956de5c7391660f753cb663dcdefca`  
		Last Modified: Wed, 15 Apr 2026 22:31:26 GMT  
		Size: 59.5 KB (59522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk8-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:dd9369473c02a6d73d734b57e8fd71f5a6828d31ed127686fcf9f1e60459b615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11657244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596558e846ab5876b5b5145441ab2116a1aed1ba8fe1818430239721c4e65ff3`

```dockerfile
```

-	Layers:
	-	`sha256:5f28fb98bda1ffa5908753602c37e8265f2626d2263ad7eb95c2d32fceb6fedc`  
		Last Modified: Wed, 15 Apr 2026 22:31:26 GMT  
		Size: 11.6 MB (11636208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9522b01e0a546718742cefa7f0aa47cb3ad52ae09b679b8860c92763248b8063`  
		Last Modified: Wed, 15 Apr 2026 22:31:25 GMT  
		Size: 21.0 KB (21036 bytes)  
		MIME: application/vnd.in-toto+json
