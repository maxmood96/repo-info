## `gradle:8-jdk17-corretto`

```console
$ docker pull gradle@sha256:9a2ba54b8bfb61ffcca49940933add090b27105049a039fe328d4ee690bc69b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:9d4aae03a1ef9fba925cba22a0e69e1dd86a718ae1d8a7e8499d43cd460393fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.0 MB (435029227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913bb0bb728b6458b4ab9c8bd9a971fee1b3f3b31b63c2262d6bcc235863bc8e`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:07 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:26:07 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:07 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:07 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 15 Apr 2026 22:17:41 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:17:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:17:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:17:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 22:17:42 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:17:42 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:17:42 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 15 Apr 2026 22:17:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 15 Apr 2026 22:17:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:17:44 GMT
USER gradle
# Wed, 15 Apr 2026 22:17:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 22:17:44 GMT
USER root
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008cbcc9cf06909dadd7713e6243b1a02925fac6d3632b00ee5b3c83554fe53c`  
		Last Modified: Wed, 15 Apr 2026 21:26:29 GMT  
		Size: 156.9 MB (156911119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298dcd6021a6fc5d3216402cd86c8c53d356b8092a70777185e8be45ab2a15df`  
		Last Modified: Wed, 15 Apr 2026 22:18:22 GMT  
		Size: 86.1 MB (86101993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c71bb357e6050eb4a6f2ff2736f4d6019ee3102d3e10f9c798f5af91ce00fe`  
		Last Modified: Wed, 15 Apr 2026 22:18:14 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1fb8b5fbf29fefc8097921b79584422012ea51fd8489e52686f9a2668ccee3`  
		Last Modified: Wed, 15 Apr 2026 22:18:23 GMT  
		Size: 137.4 MB (137388295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096437b30cc8a2235c51464c212c590a4079281c2cff4fe3e1adddc2f15cfafd`  
		Last Modified: Wed, 15 Apr 2026 22:18:14 GMT  
		Size: 54.9 KB (54888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:96c64d5b6c061062ebde09dbce800a9b97debc526d1d8584b3504f1e8cd529ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11368745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadca215c1caa91736fba12f5bb4cda2929c974805b60e13551493bc5cb0223b`

```dockerfile
```

-	Layers:
	-	`sha256:e31a443065bfb2f92177c2b9694b8ffc3f76a369d7fb6fee477d9e032de49ca1`  
		Last Modified: Wed, 15 Apr 2026 22:18:14 GMT  
		Size: 11.3 MB (11348018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd20ae673c303890acb48d8351e82388f2b5516a745082c36683b3199b3a61e9`  
		Last Modified: Wed, 15 Apr 2026 22:18:14 GMT  
		Size: 20.7 KB (20727 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:18f4a297916242c295e87d11ad11b2b7c81cb2b09d190b14c9ab0b077bcf0c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.2 MB (432223649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e227e8cffff025d8c1ed36c98af73a195d182e06adedb088c3fe6e5b618619`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:06 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:39:06 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:06 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:06 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 15 Apr 2026 22:30:10 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:30:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:30:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:30:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 22:30:10 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:30:10 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:30:10 GMT
ENV GRADLE_VERSION=8.14.4
# Wed, 15 Apr 2026 22:30:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Wed, 15 Apr 2026 22:30:13 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:30:13 GMT
USER gradle
# Wed, 15 Apr 2026 22:30:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 15 Apr 2026 22:30:14 GMT
USER root
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ece4200ddd22a4421c854fc02730d00179c130556075100cac3ac7322df40bb`  
		Last Modified: Wed, 15 Apr 2026 21:39:28 GMT  
		Size: 155.7 MB (155728403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee4a1affe00440bb8a8d57ce76eb7918a6cfbaef396101db760dc42cde31545`  
		Last Modified: Wed, 15 Apr 2026 22:30:49 GMT  
		Size: 85.6 MB (85603025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4235df8a56bfe55df878b435ae5c170b3563f5898fcda7fb51d7c6b1f1df0925`  
		Last Modified: Wed, 15 Apr 2026 22:30:45 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b106a4657f5f8950c28376db7380f6e8c5a1d2d7942d47c9baa31d38c809fc`  
		Last Modified: Wed, 15 Apr 2026 22:30:50 GMT  
		Size: 137.4 MB (137388272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4d0be3e1cd4d55f89a71cbb13ddc52a56393f50b437c500a5e2ca746203745`  
		Last Modified: Wed, 15 Apr 2026 22:30:45 GMT  
		Size: 59.5 KB (59529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:815db1244af2c18fe318b1fefaf0e3b36a4f8a491627e303668dc7dff9adcb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11367892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d041f3e51d583c25782fa629a1f129eb1c221f67c91f2627821424619bf948`

```dockerfile
```

-	Layers:
	-	`sha256:6e432e5fdbc4861746d50cd5d2d0e16d44079320a7f22402ab394adec5215188`  
		Last Modified: Wed, 15 Apr 2026 22:30:46 GMT  
		Size: 11.3 MB (11346993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e40f2e66b2203343665b0d306b042741334fb7224d5abcc3555d23057b09f23`  
		Last Modified: Wed, 15 Apr 2026 22:30:45 GMT  
		Size: 20.9 KB (20899 bytes)  
		MIME: application/vnd.in-toto+json
