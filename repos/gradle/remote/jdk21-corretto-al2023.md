## `gradle:jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:5a75f520e671ee67062f646c4315c59460069672513ba5a947042ce58f37c05c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:c3d5afab60148569677db0a633e10557fb16ee027657e14da84fe17b8309bc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.4 MB (445399094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50564f919f4a926495c3a0cc3a5eaa09747117a288beeb4bc7d9027612e52431`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:40 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:40 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:40 GMT
# ARGS: version=21.0.9.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:40 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 31 Oct 2025 01:11:33 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:11:33 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:11:33 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:11:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:11:33 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:11:33 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:11:33 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 31 Oct 2025 01:11:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 31 Oct 2025 01:11:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:11:36 GMT
USER gradle
# Fri, 31 Oct 2025 01:11:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:11:36 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b4a5d42de3c0bca4195fdbee7ccdbbaad50ab5ac755ccf13f0bd242283a472`  
		Last Modified: Fri, 31 Oct 2025 01:11:10 GMT  
		Size: 170.2 MB (170207572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0a704429a6ffb2a22d49f9c2e33416077cf141f7e730643f2413c31f2d949e`  
		Last Modified: Fri, 31 Oct 2025 01:12:49 GMT  
		Size: 85.6 MB (85611970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a640310a90706503ac4c2e3a26046561ef8da57c2563bec585bab2c7d8fcac`  
		Last Modified: Fri, 31 Oct 2025 01:12:38 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee31e100fcf8d6c4409dfa2d97d007a44f4bb9845a9569d67b69465c11a66434`  
		Last Modified: Fri, 31 Oct 2025 02:41:06 GMT  
		Size: 135.5 MB (135521732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3338502c1285102c2f15b2197d4e1aee4699198e21e674dce44c919e182b7341`  
		Last Modified: Fri, 31 Oct 2025 01:12:38 GMT  
		Size: 54.9 KB (54905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:5225be4926c48f7083800f90c3ce5631a19d5d5f554229870dcf82d6d41f87b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11337373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce776658315a6bfbca26c6e5b21fdc5f00b5b2daf31dfbccf88e6e54e65636d`

```dockerfile
```

-	Layers:
	-	`sha256:56acc5bd2095fd006996dd9eb604bc3937c91b062460356d2abeee0dc993d240`  
		Last Modified: Fri, 31 Oct 2025 02:23:33 GMT  
		Size: 11.3 MB (11315772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca3e288ffe19a42a6720200fb79ae3f8daccfc98d7c015623247dfb7db7cb03`  
		Last Modified: Fri, 31 Oct 2025 02:23:34 GMT  
		Size: 21.6 KB (21601 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:accbf39e9900788fafc9b9c4120c7cc4e324f6f2b390953f6ea5c370cabce33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.1 MB (442128318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60fde87edc4ce9bb19b0d35125ed588bcdd0542cbed6fac515149dd39398f4f7`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:57 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:57 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:57 GMT
# ARGS: version=21.0.9.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:57 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 31 Oct 2025 01:11:53 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:11:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:11:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:11:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:11:53 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:11:54 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:11:54 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 31 Oct 2025 01:11:54 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 31 Oct 2025 01:11:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:11:56 GMT
USER gradle
# Fri, 31 Oct 2025 01:11:57 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:11:57 GMT
USER root
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed77e24e263615113568f971380ee95108409043a4dc2ccda5b462e834b7a960`  
		Last Modified: Fri, 31 Oct 2025 01:11:28 GMT  
		Size: 168.5 MB (168475202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad80bfbd680c22992af0eba09d0888f4047d170609c4d579e5d38a32739101e`  
		Last Modified: Fri, 31 Oct 2025 01:12:42 GMT  
		Size: 85.2 MB (85168325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547810f5c2dc1ceeed205de87c008d12315a5012eafd65cc46ace7aad6545626`  
		Last Modified: Fri, 31 Oct 2025 01:12:36 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347554a35c5cca841b4e10add4654bde37e4088458d9304286edd4bcfdb6c3d3`  
		Last Modified: Fri, 31 Oct 2025 01:12:31 GMT  
		Size: 135.5 MB (135521731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1994c04d68f313205f31184678b1440d1899b86df8c94d05bed18f0b79a6905`  
		Last Modified: Fri, 31 Oct 2025 01:12:36 GMT  
		Size: 59.5 KB (59531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:309ce7dc65d4e9cbd9a741d932fdf4d7c5db6498258d03637fe90d0e8215db58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11336573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e4e277a5544cfe1a660504aec12b4f346856c9fedd0b007e3d3529cb56bb46`

```dockerfile
```

-	Layers:
	-	`sha256:b7bc6c89ed6af700c15b3ecd0e0e311a23ada18927d9e68e64adce35e76c6e7e`  
		Last Modified: Fri, 31 Oct 2025 02:23:44 GMT  
		Size: 11.3 MB (11314774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a7ba4bf0d89269d082aaf3ea7cbc57485f42dd7cb51193e5a4f1b94416f1f7`  
		Last Modified: Fri, 31 Oct 2025 02:23:45 GMT  
		Size: 21.8 KB (21799 bytes)  
		MIME: application/vnd.in-toto+json
