## `gradle:jdk17-corretto`

```console
$ docker pull gradle@sha256:32827e354d909dd003ea4f6a18bc9c650d343594dae1dc2b9bd10d75d88efeb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:8b23515438ea97fc7da20cf4b7c9a7971aa9957dec7050787eb94561a4d9cf3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.4 MB (435416473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f387abf16cfd5ff1ef2a2011013283c4b005b5934e7f420ff931d51c57442e2c`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:36 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:14:36 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:36 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:36 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 23:11:54 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:11:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:11:54 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:11:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:11:54 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:11:55 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:11:55 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 03 Apr 2026 23:11:55 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 03 Apr 2026 23:11:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:11:57 GMT
USER gradle
# Fri, 03 Apr 2026 23:11:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 03 Apr 2026 23:11:57 GMT
USER root
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa6c65371a2d0452e68a7849e65aa6fec9a2eacabd234c5f9ae4305aa623f8e`  
		Last Modified: Fri, 03 Apr 2026 22:14:58 GMT  
		Size: 156.9 MB (156911184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c6f5cbe142d412e6ed437f6509c8006d603cf989c2f3496e661afb4f515d7c5`  
		Last Modified: Fri, 03 Apr 2026 23:12:28 GMT  
		Size: 86.1 MB (86098374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89018ed0390f490b679082c7f7df5b8bd2f486f75f8c5362b72be0b290d2b945`  
		Last Modified: Fri, 03 Apr 2026 23:12:24 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef103a43df1b37a2fe99a573ae17858491ecfbf7520124d825f1ffb4e88ef21`  
		Last Modified: Fri, 03 Apr 2026 23:12:30 GMT  
		Size: 137.8 MB (137808330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469a72ebb4b01b4265d62e3a30d8ef6e996fc76d8a8a3a963b3fdd4b7a4b2d27`  
		Last Modified: Fri, 03 Apr 2026 23:12:24 GMT  
		Size: 25.6 KB (25604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:a8e060c7f60f21d44fd19163ea104c4c7ac7a1ca987c0fd65929788f97120418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11355918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21b371de8088f164612696b9f2ff81fef92f4ea319d8cddf49b2c817afb130f`

```dockerfile
```

-	Layers:
	-	`sha256:48875170571d9c5e41df9b0ebcd3e0ae17ce20667822ed2861ce5d0541d1ea01`  
		Last Modified: Fri, 03 Apr 2026 23:12:24 GMT  
		Size: 11.3 MB (11334421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c80790be4b8c7fafa22bb88a467194c314ae25f126d8a7061f5ae66937632e3`  
		Last Modified: Fri, 03 Apr 2026 23:12:24 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ad937e3846131c19d2f2683b9250ac0be4d80957b50eb0eb555975ac403fe796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.6 MB (432615432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a067508d23e6289e6b755e8ca8d37aad9dc8c7ea96dc800ca5921fe71a6941e`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:52:42 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:52:42 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:52:42 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:52:42 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:52:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 03 Apr 2026 23:12:25 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 23:12:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 23:12:25 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 23:12:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 23:12:26 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 23:12:26 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 23:12:26 GMT
ENV GRADLE_VERSION=9.4.1
# Fri, 03 Apr 2026 23:12:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Fri, 03 Apr 2026 23:12:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 23:12:28 GMT
USER gradle
# Fri, 03 Apr 2026 23:12:29 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Fri, 03 Apr 2026 23:12:29 GMT
USER root
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a171146ed2608cfed7379a8e096372cbf936c9d64c321d3b501ba505f2694fb8`  
		Last Modified: Fri, 03 Apr 2026 22:53:07 GMT  
		Size: 155.7 MB (155728253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536ecfd43e403e39d495bdb56cd9fdf19680996fec35abc8605ede4803dffbdc`  
		Last Modified: Fri, 03 Apr 2026 23:13:01 GMT  
		Size: 85.6 MB (85605007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ac922e6c6bad1ed4df093d10c09d9cf2ba577160cb5eefbe80f4a787f7952b`  
		Last Modified: Fri, 03 Apr 2026 23:12:57 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eee65908b1d37bccfd70dd3fe578dab4f7bd8326641ab41a2301748ef6204fe`  
		Last Modified: Fri, 03 Apr 2026 23:13:02 GMT  
		Size: 137.8 MB (137808333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:449dea7cf3e907e47490648446fbb265868a124a4b167da8ce766f2560c18942`  
		Last Modified: Fri, 03 Apr 2026 23:12:57 GMT  
		Size: 29.3 KB (29332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:592079b4fe31407bcb2322c828a171020c784161d8872f4530b9ca1980bee7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11355114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36de32da35db632efbe93a0ee934fa53d50ce4487fd95bc46ced0bc688605c1`

```dockerfile
```

-	Layers:
	-	`sha256:d58b991775bf28b177e50721d2224b65d9cc2a9df97427d771532738f1433f7b`  
		Last Modified: Fri, 03 Apr 2026 23:12:58 GMT  
		Size: 11.3 MB (11333420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:259a5e2b383afde0d403d5593eaa48e090af14dcd0016c568364d763d5d85c6a`  
		Last Modified: Fri, 03 Apr 2026 23:12:57 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
