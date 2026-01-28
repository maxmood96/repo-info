## `gradle:jdk25-corretto-al2023`

```console
$ docker pull gradle@sha256:21101a0ab32656ccc33baf431d30ecf8eba9e3d0d157fa5b26f55dc5662af4df
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk25-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:2afd9dea47e9d54083dcb189d48db6fda4a84b028288cbd6afb35de2e03738c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.3 MB (466266522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3593ab34244777b1ee38e6f185c43620f696b5c0858922df5e49afc88493b515`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:13:36 GMT
ARG version=25.0.2.10-1
# Tue, 27 Jan 2026 22:13:36 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:13:36 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:13:36 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:13:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 27 Jan 2026 23:12:04 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:12:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:12:04 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 Jan 2026 23:12:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 Jan 2026 23:12:04 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 Jan 2026 23:12:04 GMT
WORKDIR /home/gradle
# Tue, 27 Jan 2026 23:12:04 GMT
ENV GRADLE_VERSION=9.3.0
# Tue, 27 Jan 2026 23:12:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Tue, 27 Jan 2026 23:12:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:12:07 GMT
USER gradle
# Tue, 27 Jan 2026 23:12:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 27 Jan 2026 23:12:07 GMT
USER root
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9307319cf5c73e99e04dcd81f4b9092ff8c453a217e95ba5b67ed0628f3138`  
		Last Modified: Tue, 27 Jan 2026 22:14:01 GMT  
		Size: 189.2 MB (189191158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f74cca565f38648ec9f0d83a50bd2850836e00e2867455fa4653a9cb32a55dc`  
		Last Modified: Tue, 27 Jan 2026 23:12:38 GMT  
		Size: 86.0 MB (86035387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b785536c7024172dddd7c007f046282b0a5f5705856b0d14ff21543767001a8`  
		Last Modified: Tue, 27 Jan 2026 23:12:34 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e6f10893cdb05d7ee6ee6652083711e622123dbcc42bc2f9930a5ce86fc5f1`  
		Last Modified: Tue, 27 Jan 2026 23:12:39 GMT  
		Size: 137.0 MB (136988868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0afc5156c82017f157e09ced7fe1e2c00c2efab5799331e940b3dea83091d2`  
		Last Modified: Tue, 27 Jan 2026 23:12:34 GMT  
		Size: 25.6 KB (25594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:ed3a31b48c2347181968ac67f4a1430652cc80b54ce802db205b02c6dac134d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11360580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff2399cda4a448b52d1c0c272b987ab99fdc87582c431a15c2ada74b6ac5352`

```dockerfile
```

-	Layers:
	-	`sha256:9bf4fc7e9b23ca9c255991df668a23cdb3140316be975db208f6b6794ef65785`  
		Last Modified: Tue, 27 Jan 2026 23:12:35 GMT  
		Size: 11.3 MB (11338311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dda5c654495029e6e569771d035493695e5d0c0edc48ec6e185ac11d79d422d8`  
		Last Modified: Tue, 27 Jan 2026 23:12:34 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk25-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8c581ca42ad30458918f60756031ed54caa09e312b387b0814ec79c0adb030d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **462.5 MB (462541719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40df59480e49f5ee845f66c73240615434a4d2df31038f2b6ada7a25eeb1b3a0`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 27 Jan 2026 21:24:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:24:49 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:56 GMT
ARG version=25.0.2.10-1
# Tue, 27 Jan 2026 22:12:56 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:12:56 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:56 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 27 Jan 2026 23:12:06 GMT
CMD ["gradle"]
# Tue, 27 Jan 2026 23:12:06 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 27 Jan 2026 23:12:06 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 27 Jan 2026 23:12:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 27 Jan 2026 23:12:06 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 27 Jan 2026 23:12:06 GMT
WORKDIR /home/gradle
# Tue, 27 Jan 2026 23:12:06 GMT
ENV GRADLE_VERSION=9.3.0
# Tue, 27 Jan 2026 23:12:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
# Tue, 27 Jan 2026 23:12:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 27 Jan 2026 23:12:09 GMT
USER gradle
# Tue, 27 Jan 2026 23:12:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=0d585f69da091fc5b2beced877feab55a3064d43b8a1d46aeb07996b0915e0e0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 27 Jan 2026 23:12:09 GMT
USER root
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af45d8028ea21d913fa4bbb3381bedf24377df2182daab5e8ed011f7165bbfd`  
		Last Modified: Tue, 27 Jan 2026 22:13:21 GMT  
		Size: 187.1 MB (187091178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207141d2123181f4a138b3134c4a99e3e1e2c3db20e88b496896242ded51d809`  
		Last Modified: Tue, 27 Jan 2026 23:12:41 GMT  
		Size: 85.5 MB (85514040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:220fa28942bfc74c2814f429e093284afeff9ea35d368b4ab912789e924eac35`  
		Last Modified: Tue, 27 Jan 2026 23:12:37 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cd77e500e1925a8d30bbc9e1efa86c3f5100a7fbde36dc77aa41f96a0ce7aa`  
		Last Modified: Tue, 27 Jan 2026 23:12:41 GMT  
		Size: 137.0 MB (136988869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abff0618ca3d23cf2234d7256910e67d5df0a70f92693ec98e6cf701f68add9a`  
		Last Modified: Tue, 27 Jan 2026 23:12:37 GMT  
		Size: 29.3 KB (29315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk25-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:7b2e6971e870ee920d2308801e41a832ba6617beb770568e768b274a1b69b8ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11359838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98078509b403de828d6834e57fb67170226b907468eb078f9064364fee800fa8`

```dockerfile
```

-	Layers:
	-	`sha256:1441f3b39794504e3c5e29854ffb68f23be2d9e70635557365e7a4aed6658ab3`  
		Last Modified: Tue, 27 Jan 2026 23:12:38 GMT  
		Size: 11.3 MB (11337348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0e6bdc5a36955a247a7fd06499d60392da76c2b35f46db46f799437977e4813`  
		Last Modified: Tue, 27 Jan 2026 23:12:37 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
