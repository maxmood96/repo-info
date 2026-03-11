## `gradle:8-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:982028f59e0f28fcfa039da9b2377e95370cfdd89b310e8a40e94b3ce6d83ae7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:56d90f952c2796e4b711ad8463f71669b64b6eaa980831737f19f46618d173e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447740237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25b79fca8b2e61c91ec6a34d70a31dc0e9b73fed843bca5aff0f68026559139`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:01 GMT
ARG version=21.0.10.7-1
# Wed, 11 Mar 2026 18:34:01 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:01 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:01 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 11 Mar 2026 19:13:05 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:13:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:13:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 11 Mar 2026 19:13:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 11 Mar 2026 19:13:05 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:13:06 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:13:06 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 11 Mar 2026 19:13:06 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 11 Mar 2026 19:13:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:13:08 GMT
USER gradle
# Wed, 11 Mar 2026 19:13:09 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 11 Mar 2026 19:13:09 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f515facfbc58fdfaa9cdcbd4b5a55791c80be6edda4df3bb9183ca525b464ed`  
		Last Modified: Wed, 11 Mar 2026 18:34:23 GMT  
		Size: 170.2 MB (170192431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9af29f0ec23780f52d939ca68271ba633fc7b6869a3a6689e7dcf04046f400`  
		Last Modified: Wed, 11 Mar 2026 19:13:37 GMT  
		Size: 86.1 MB (86069861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cd501b57a4c818e3517da816951aae7ba7526ab7e22f9b840081c34ab2fe87`  
		Last Modified: Wed, 11 Mar 2026 19:13:33 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22b6eb4becca6b3e84e41277665d1775d64beb1195a858ddda9360f4007d8df`  
		Last Modified: Wed, 11 Mar 2026 19:13:39 GMT  
		Size: 137.4 MB (137388268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba6362999193eb937bda6696205d69e9a79195bf53dba7a893449ff46cb6363`  
		Last Modified: Wed, 11 Mar 2026 19:13:34 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:a2be45657c15be2633a25f08e0f9c61fd7617ec3bdfc90ca7f4b5a0416ea6112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11363236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05547989ee1b922c793d6e7052dd8935a29988236407e7de4e4da5c88637dafd`

```dockerfile
```

-	Layers:
	-	`sha256:ed6f1bc24702a461e297a641415a892b59e39cb7c2202e7fc875953a064f925a`  
		Last Modified: Wed, 11 Mar 2026 19:13:34 GMT  
		Size: 11.3 MB (11342355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d66b34689a74cd67e192007d11d98cc31902ba9051098b247fd6119032b76f5`  
		Last Modified: Wed, 11 Mar 2026 19:13:33 GMT  
		Size: 20.9 KB (20881 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:db1a1f97dc9ab6c1948c6fc0d0fabc2b21684816f898c8642a146e9f0d11cc47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.4 MB (444399414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad52cfd8a5cdfa0837d8d3a7f2e8273f7fca47779462b177770f7ec029c7e7e8`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:49 GMT
ARG version=21.0.10.7-1
# Wed, 11 Mar 2026 18:33:49 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:33:49 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:33:49 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 11 Mar 2026 19:13:04 GMT
CMD ["gradle"]
# Wed, 11 Mar 2026 19:13:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 11 Mar 2026 19:13:04 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 11 Mar 2026 19:13:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 11 Mar 2026 19:13:04 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 11 Mar 2026 19:13:04 GMT
WORKDIR /home/gradle
# Wed, 11 Mar 2026 19:13:04 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 11 Mar 2026 19:13:04 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 11 Mar 2026 19:13:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 11 Mar 2026 19:13:07 GMT
USER gradle
# Wed, 11 Mar 2026 19:13:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 11 Mar 2026 19:13:07 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d30746b1d1a0fa8e3ef2fe5cc5ec2c6c146413028b9dd25386bd91e4b836e`  
		Last Modified: Wed, 11 Mar 2026 18:34:14 GMT  
		Size: 168.5 MB (168466825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260d90c1143793ff134cdcd168c5f90b3146869e39765861dcbb00e5c4d244a4`  
		Last Modified: Wed, 11 Mar 2026 19:13:38 GMT  
		Size: 85.5 MB (85541742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4fae252dfe834788744df1fa81a3e1413aa0a3e3047a316a9a7c433e8209bf9`  
		Last Modified: Wed, 11 Mar 2026 19:13:35 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31c46a7a49ded71de1739ba9a19af0080d591827da99ea35bf5edf370225237`  
		Last Modified: Wed, 11 Mar 2026 19:13:39 GMT  
		Size: 137.4 MB (137388267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f9fee3fe7c65d0610aac3709cf33d7f1022cde7c6cb391d26cd1a6fa95bf1b`  
		Last Modified: Wed, 11 Mar 2026 19:13:35 GMT  
		Size: 59.5 KB (59527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:3b2f2a864f81478b8fb239e06009c1ccd34f6ceda40e8ac0c39f655f30df86f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11362387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eaf190a7034a025f3ede9126b04931a342c74a9cd67d2721110f8b3d378e5c1`

```dockerfile
```

-	Layers:
	-	`sha256:5f918635aa1abff2da86c85b7ba299ab1e51678c1aa34779a107395eb85e3454`  
		Last Modified: Wed, 11 Mar 2026 19:13:36 GMT  
		Size: 11.3 MB (11341333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c43104478fe97c4710db2bba6f69fdca121dce87cb1ced925f827f6f2bf1c0`  
		Last Modified: Wed, 11 Mar 2026 19:13:35 GMT  
		Size: 21.1 KB (21054 bytes)  
		MIME: application/vnd.in-toto+json
