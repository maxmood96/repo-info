## `gradle:8-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:28b7bda89568dbc028b37bab3fd5dce7b8bb45e3ec700d661c4900b86cfa5621
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:e06209786d2fcec773a86ad1855c4b2572ed75d590f50d76d42defd9113e970b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.1 MB (436118149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beab7dfe9bb5d7c29aa829dfd3b4918c815002a0979067a790f5fd10ed1678a3`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:15:28 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:15:28 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:15:28 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:15:28 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:15:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 16 Jun 2026 02:19:41 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 02:19:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 02:19:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 16 Jun 2026 02:19:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 02:19:42 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 02:19:42 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 02:19:42 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 16 Jun 2026 02:19:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 16 Jun 2026 02:19:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 02:19:44 GMT
USER gradle
# Tue, 16 Jun 2026 02:19:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 02:19:45 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cbe16b91281bbab0f677616f852468a1efb463957ba2554f568b2f9ac583b3`  
		Last Modified: Tue, 16 Jun 2026 01:15:51 GMT  
		Size: 157.2 MB (157156724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c308b437c27ebb92c859379fbef427ae8ffb76c61dea1ee8591485bf07a9eb84`  
		Last Modified: Tue, 16 Jun 2026 02:20:16 GMT  
		Size: 86.3 MB (86265124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fb056fafaeb9549bc2124d830dad41d1938eb84de211c3fc3df867b58e66b5`  
		Last Modified: Tue, 16 Jun 2026 02:20:13 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378aa5dfe6428c4cc42b43b1f204a88e847da7c7d5dd908dba729bb61b24f0e6`  
		Last Modified: Tue, 16 Jun 2026 02:20:18 GMT  
		Size: 138.1 MB (138068561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf7ff9ac23abc2fd4c3b80925cc3206ebad5d13133c06170721639f12b0ce80`  
		Last Modified: Tue, 16 Jun 2026 02:20:13 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:8149c8c01e251fc1dc145bcd23978cc73feccb5b965479d2b2ed14958dfda00a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11371197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220b4a2967535152bfe66792384794b0293edadc69c8800ed67ba1fa6c21bbc1`

```dockerfile
```

-	Layers:
	-	`sha256:fd4ce4ec5f7ea5cfce8701646dcbf67c5a92974eadf97473c9248f52b0cf36fb`  
		Last Modified: Tue, 16 Jun 2026 02:20:13 GMT  
		Size: 11.4 MB (11350332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6def70a8520c2f02c2a6d2a94b3c0e7941c8a7d6e3bf97cddc4c83874576f29c`  
		Last Modified: Tue, 16 Jun 2026 02:20:13 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:76ac3ff419b8aef471f53e8de5296923528dcce9f3b76aaa0ad98d6c49f10724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.3 MB (433296927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840aec29a6f9c667e431c5f37e7e2733c975611b50fcf46be912ace277b1d5f9`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:35 GMT
ARG version=17.0.19.10-1
# Tue, 16 Jun 2026 01:16:35 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:16:35 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:16:35 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 16 Jun 2026 02:20:22 GMT
CMD ["gradle"]
# Tue, 16 Jun 2026 02:20:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 16 Jun 2026 02:20:22 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 16 Jun 2026 02:20:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 16 Jun 2026 02:20:22 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 16 Jun 2026 02:20:22 GMT
WORKDIR /home/gradle
# Tue, 16 Jun 2026 02:20:22 GMT
ENV GRADLE_VERSION=8.14.5
# Tue, 16 Jun 2026 02:20:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
# Tue, 16 Jun 2026 02:20:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 16 Jun 2026 02:20:25 GMT
USER gradle
# Tue, 16 Jun 2026 02:20:25 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=6f74b601422d6d6fc4e1f9a1ab6522f642c2fdcbc15ae33ebd30ba3d7198e854
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 16 Jun 2026 02:20:25 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25f04afa63e84df40811c8b1eb43c711fcfea0a157148dfba69328e8dc1769f`  
		Last Modified: Tue, 16 Jun 2026 01:16:57 GMT  
		Size: 156.0 MB (155987128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f50ab6b2ad58af760ab36c304dd394351e5d40c966ae3792e2eb7c4ee5872c`  
		Last Modified: Tue, 16 Jun 2026 02:20:56 GMT  
		Size: 85.7 MB (85722242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a4adee72c844872c35ce67be4ab9e52eacf5174d9f06c19757bdc18fd56087`  
		Last Modified: Tue, 16 Jun 2026 02:20:53 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2dd02d88af9be9499f72c62039c2ee7378b0e4c9629ddf3ec448522a39b637`  
		Last Modified: Tue, 16 Jun 2026 02:20:57 GMT  
		Size: 138.1 MB (138068535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52209a05187126d9187310d259cf3c2c713425b062869cc0cce1bd0a04efc29a`  
		Last Modified: Tue, 16 Jun 2026 02:20:53 GMT  
		Size: 59.5 KB (59518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:d7b7141c390afea12282a121dbe88f4709e46051f95de9334d16b427ff8c5377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11370346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f829a9f79d3746295b99adb23fd1454511771d2b102d85e1ecf116a20b08cd22`

```dockerfile
```

-	Layers:
	-	`sha256:a029b12fa51ea74a56ce0a3911187c37d8b862b342e4daeef2bc7479095bb85e`  
		Last Modified: Tue, 16 Jun 2026 02:20:54 GMT  
		Size: 11.3 MB (11349308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7735c5849586dfc36a83b2af5ee02b62ea74575e1f8df79f2efa2735157404`  
		Last Modified: Tue, 16 Jun 2026 02:20:53 GMT  
		Size: 21.0 KB (21038 bytes)  
		MIME: application/vnd.in-toto+json
