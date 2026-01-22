## `gradle:7-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:373325cd9096db9702c17feec6ccf8f2c1237f440b50ad57957238af090f2fb6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:8c9fbc2540eb491dd9d955a5399ada774f664eb3926ec454c492235e68cf7a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.5 MB (425497802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ce374651f8b316e877e689f014c34c9dd66052ef67ac8196405a92695da030`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:24 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 18:59:24 GMT
ARG package_version=1
# Wed, 21 Jan 2026 18:59:24 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:24 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:17:14 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:17:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:17:14 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:17:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:17:14 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:17:14 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:17:14 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 21 Jan 2026 19:17:14 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 21 Jan 2026 19:17:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:17:16 GMT
USER gradle
# Wed, 21 Jan 2026 19:17:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 21 Jan 2026 19:17:17 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9611f4d384734b62e775c9d6504436549d04bb86a1c85fb4d696880e755c9a`  
		Last Modified: Wed, 21 Jan 2026 18:59:47 GMT  
		Size: 156.9 MB (156916086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b2cd144687ac5e4c200b10a5dc43ac98c320e51e5d400a6a4f0434e06a3b1d`  
		Last Modified: Wed, 21 Jan 2026 19:17:48 GMT  
		Size: 86.0 MB (86034509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695b1d23da7de0fb97a4889a7ad19fe1375451cf17f679e68381d67ee90e2d04`  
		Last Modified: Wed, 21 Jan 2026 19:17:44 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c2d694887f005e77213571eef2bbced020e4a5abf54156324112b709208f6c`  
		Last Modified: Wed, 21 Jan 2026 19:17:49 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b87a147743fafb21b768a77c29bdaa39bd6b66327a9071c8c1e3c963af10d4d`  
		Last Modified: Wed, 21 Jan 2026 19:17:44 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:55b48bf870cee13fd3d370770c0bedb2620ce00a181f6dfde19e7207511aaa1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11271178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc278171de00f15eab616ce51bb52b6f5414df34b6ac68797639373c0e8a523`

```dockerfile
```

-	Layers:
	-	`sha256:bd3149776ce60bb64686e97ec701e995743b4792e04931ee001497ddab1c074c`  
		Last Modified: Wed, 21 Jan 2026 19:17:45 GMT  
		Size: 11.3 MB (11250465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52423a248cd111253583e43bcbbbc24ea6396cd82387b2607435b04c60983e32`  
		Last Modified: Wed, 21 Jan 2026 19:17:44 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6ed7213183cae836de1e1b40bfc3486098c808925b94a4121a33056f5c4a6c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.7 MB (422679601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00727fa93a48e1dddb76854d479d899952b8786902910cef9fea107ec3d9cad0`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:37 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:37 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:00:37 GMT
# ARGS: version=17.0.18.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:00:37 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 21 Jan 2026 19:18:07 GMT
CMD ["gradle"]
# Wed, 21 Jan 2026 19:18:07 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 21 Jan 2026 19:18:07 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 21 Jan 2026 19:18:07 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 21 Jan 2026 19:18:07 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 21 Jan 2026 19:18:07 GMT
WORKDIR /home/gradle
# Wed, 21 Jan 2026 19:18:07 GMT
ENV GRADLE_VERSION=7.6.6
# Wed, 21 Jan 2026 19:18:07 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Wed, 21 Jan 2026 19:18:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 21 Jan 2026 19:18:10 GMT
USER gradle
# Wed, 21 Jan 2026 19:18:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 21 Jan 2026 19:18:11 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e98527feec5a6e3b7d9dd4edae394a807158bda7cdb1fdad45eafe42104a93`  
		Last Modified: Wed, 21 Jan 2026 19:01:02 GMT  
		Size: 155.7 MB (155718940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b13e15113fad3d97fe84a209947faf64ff95fa0d5586f76e843055ddf543755`  
		Last Modified: Wed, 21 Jan 2026 19:18:42 GMT  
		Size: 85.5 MB (85515692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8372926510db76c39f913490b566a9b1c622fcfae70a22e0f4bf7af753e76651`  
		Last Modified: Wed, 21 Jan 2026 19:18:38 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2633bc8ec4cb5bc8615b9cadce86154f0ced1980bab828e142454f0040be86`  
		Last Modified: Wed, 21 Jan 2026 19:18:43 GMT  
		Size: 128.5 MB (128469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a367d0a24993247f087f747ad3d4419f66f9dd5760f92aa28b2187814c867004`  
		Last Modified: Wed, 21 Jan 2026 19:18:39 GMT  
		Size: 59.5 KB (59515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:0289efb9cb2f9e7faddb23e3046b3e9d715d6d37ae6a4c254db984422420ef83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11270330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac40e511d74d8852f70b3326e94a6b44d5107384ebce7db8d1abfbae9e790ecb`

```dockerfile
```

-	Layers:
	-	`sha256:addd4e7bfcd449d4d49303690d645e7683a039c5d10c82ce657ff74c21f5a1f8`  
		Last Modified: Wed, 21 Jan 2026 19:18:39 GMT  
		Size: 11.2 MB (11249444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:128f769ec5f3d8a8b2477ffdb39f198d06968f5be31fe74d88f25563638bf7a2`  
		Last Modified: Wed, 21 Jan 2026 19:18:38 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
