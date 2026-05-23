## `gradle:7-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:9e3f248a2497a398cc3b0284a4bb9304806b853fe114e508565e08e7e6db472a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:c21b61100ecab03235efde965e15b25f519fe21f2f72f936bd5c7ac7101db71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **426.4 MB (426446770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5284682be9037c6d83cffb5f8cc6a5e6f003c7f307d6b606bf178320e4910af9`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:37 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:37 GMT
ARG package_version=1
# Fri, 22 May 2026 21:11:37 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 22 May 2026 22:06:33 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:06:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:06:33 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:06:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:06:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:06:33 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:06:33 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 22 May 2026 22:06:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 22 May 2026 22:06:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:06:35 GMT
USER gradle
# Fri, 22 May 2026 22:06:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 22 May 2026 22:06:36 GMT
USER root
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6459ce5e246b3d8bb1803ab05d270e314eb5e96858a505646b82833ddd5121`  
		Last Modified: Fri, 22 May 2026 21:11:57 GMT  
		Size: 157.2 MB (157158594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b531884aedc382f1012d1f86178433ce5cbf6511a053200bbdcc2203a1ddc95`  
		Last Modified: Fri, 22 May 2026 22:07:05 GMT  
		Size: 86.2 MB (86189733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f2860b80aa038a532bf3813269f7687f44fbf87de6357eb1b36a4ff271d5d2`  
		Last Modified: Fri, 22 May 2026 22:07:02 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2e6120e44b7b7af31465433cdcd0719474917c00269049304b1991665e343a`  
		Last Modified: Fri, 22 May 2026 22:07:06 GMT  
		Size: 128.5 MB (128469416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8a09c77048cce2731f12b75776c420cb08ce114819202d2098fcad610e04ef`  
		Last Modified: Fri, 22 May 2026 22:07:02 GMT  
		Size: 54.9 KB (54906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:80e1612ea2f658cebe91c05cfc0f54cf92a4e2ce12ebfd3fed645ff22e20106c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11281699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a3665d6b7c14d6502ad01d1e890b6fe6fd83e2e7c0a6ae2d25136dbbae4905`

```dockerfile
```

-	Layers:
	-	`sha256:b758dbe5d264053dfc029c03833cb9dabf1e07cdcc116b19fb12a5f477a21297`  
		Last Modified: Fri, 22 May 2026 22:07:03 GMT  
		Size: 11.3 MB (11260987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5f70606633b526f6b21974db9bf54854e9a05c58e64d2578fd0c3751d7a6cd`  
		Last Modified: Fri, 22 May 2026 22:07:02 GMT  
		Size: 20.7 KB (20712 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:3dbf67d27f7b7af02478c4f7c3065a79b7d648165c386641f923a1170e6a6c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.7 MB (423667588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af49a4baee022e62240d4dc7d19172d81efd0f9709678cb4284d9eb0727c3f6e`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:33 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:33 GMT
ARG package_version=1
# Fri, 22 May 2026 21:11:33 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:33 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 22 May 2026 22:07:44 GMT
CMD ["gradle"]
# Fri, 22 May 2026 22:07:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 22 May 2026 22:07:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 22 May 2026 22:07:45 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 22 May 2026 22:07:45 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 22 May 2026 22:07:45 GMT
WORKDIR /home/gradle
# Fri, 22 May 2026 22:07:45 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 22 May 2026 22:07:45 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 22 May 2026 22:07:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 22 May 2026 22:07:47 GMT
USER gradle
# Fri, 22 May 2026 22:07:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 22 May 2026 22:07:48 GMT
USER root
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76dff99f7dfb9e95ce331867dbe7cc08952add0452592bfbccd1c64d2711416`  
		Last Modified: Fri, 22 May 2026 21:11:55 GMT  
		Size: 156.0 MB (155987820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b353dedeb33a8ab2d8fff1acdc662087eb6d570114599476e9ccb13684f4236`  
		Last Modified: Fri, 22 May 2026 22:08:17 GMT  
		Size: 85.7 MB (85694735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0b423816d31616dc55729e5d1baef963505542afa5e4f7ac60ae17b5c8e918`  
		Last Modified: Fri, 22 May 2026 22:08:13 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442f38478d6c4c68f6dd872b34850d1c4b8c8404a14dcadec122f5afa16ca7c4`  
		Last Modified: Fri, 22 May 2026 22:08:18 GMT  
		Size: 128.5 MB (128469415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896745596df341d5ead14ebb4ee0289452743a3e7383d1b73f842c118e6a7f59`  
		Last Modified: Fri, 22 May 2026 22:08:14 GMT  
		Size: 59.5 KB (59523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:dcb2b23769ea436434578516bfe51ee89cb04559963f2e29105f22d192c948c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11280849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f85d0af661df06b2a2a2070dfd011eaae7811fa3452308f9d369a31b84e7494`

```dockerfile
```

-	Layers:
	-	`sha256:85f27cb18d4024b39812df43a915899674822bd28800314cc4e7ba10ea83f90e`  
		Last Modified: Fri, 22 May 2026 22:08:14 GMT  
		Size: 11.3 MB (11259963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c10eda4d701f71b414f36f80a36d0b94233441b43694c381670cb33018b89bd3`  
		Last Modified: Fri, 22 May 2026 22:08:13 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
