## `gradle:7-jdk17-corretto`

```console
$ docker pull gradle@sha256:78a207b71de0c3825927d36b05ac4b33bb97151ce3a8fd709ad5842e3376fd71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:26561ad318e30912ab9cec7718c055035340e352ae54b752a2e7f8373b6e2140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.1 MB (425071967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02baa4073cf16af688f4a8079b81e4fff8295d2a375d802fd12a5c33de53e6aa`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:05 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:05 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:05 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:05 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 31 Oct 2025 01:12:00 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:12:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:12:00 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:12:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:12:00 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:12:01 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:12:01 GMT
ENV GRADLE_VERSION=7.6.6
# Fri, 31 Oct 2025 01:12:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Fri, 31 Oct 2025 01:12:03 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:12:03 GMT
USER gradle
# Fri, 31 Oct 2025 01:12:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:12:04 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc93996f720aafe561378567487aad4cac58bd5c93215d7c30b4dc3cb269fe7d`  
		Last Modified: Fri, 31 Oct 2025 01:11:05 GMT  
		Size: 156.9 MB (156930995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1cb937a46287ae2f6c6c96f4e158cad7da8613f0520df8ba95bbb744caa6e1`  
		Last Modified: Fri, 31 Oct 2025 01:12:51 GMT  
		Size: 85.6 MB (85613711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3b851ab21df984b157cacb14b00c50178f0c1ba25ff9ba25541f462aef0708`  
		Last Modified: Fri, 31 Oct 2025 01:12:39 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e748becf97dfaa0a1c4915f380913bb624a40230436730670a6be38cfc2ad5`  
		Last Modified: Fri, 31 Oct 2025 03:43:40 GMT  
		Size: 128.5 MB (128469443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd250c0020a6389a264101ff43dde57e9c4e989decf48b047918f777a24fc135`  
		Last Modified: Fri, 31 Oct 2025 01:12:39 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c5fbfda8424061eabfc83851a5ee868d8669b4ba7e3c869c0287997ee37ab9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11249804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c79590e16b13621aa68c003259cefe68cbd1a3f64e189cf1cf2b441eaabcab`

```dockerfile
```

-	Layers:
	-	`sha256:91e10575182707ecca0ce5c3223e469812194bf89ec1946a4d0afc9a742b6ae6`  
		Last Modified: Fri, 31 Oct 2025 02:18:49 GMT  
		Size: 11.2 MB (11229091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b223dd778066477428e55cceae07178cd3518565f475ceb2275cbd5dcae19052`  
		Last Modified: Fri, 31 Oct 2025 02:18:49 GMT  
		Size: 20.7 KB (20713 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6a6762a174529062d60770c8d8ab33626031ef0d9381e3ece0e858e509170341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.3 MB (422341032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479e8ec121aed8e517c4540e4774aabc2bf55390b2832333ebb6c7f872edff8f`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:29 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 22:13:29 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:13:29 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:13:29 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 06 Nov 2025 23:13:05 GMT
CMD ["gradle"]
# Thu, 06 Nov 2025 23:13:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 06 Nov 2025 23:13:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 06 Nov 2025 23:13:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 06 Nov 2025 23:13:05 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 06 Nov 2025 23:13:05 GMT
WORKDIR /home/gradle
# Thu, 06 Nov 2025 23:13:05 GMT
ENV GRADLE_VERSION=7.6.6
# Thu, 06 Nov 2025 23:13:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
# Thu, 06 Nov 2025 23:13:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 06 Nov 2025 23:13:08 GMT
USER gradle
# Thu, 06 Nov 2025 23:13:08 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=673d9776f303bc7048fc3329d232d6ebf1051b07893bd9d11616fad9a8673be0
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 06 Nov 2025 23:13:08 GMT
USER root
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42206444f43ddda96491ceb64db5c92fe941fa16f8ddf5f9800eaf678742c975`  
		Last Modified: Thu, 06 Nov 2025 23:11:31 GMT  
		Size: 155.7 MB (155740957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcc45f766f628a5cd0328984116da23d5658a4a7abf13cba66c35ea20053cc6`  
		Last Modified: Thu, 06 Nov 2025 23:14:01 GMT  
		Size: 85.2 MB (85167770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c84b02ce61a6c3506e1261a54f05091f209801ef0e5e9c1cb03357fc2186b4`  
		Last Modified: Thu, 06 Nov 2025 23:13:53 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b438a726451ddc98d2330ad8406fef88123760e63c0d712fe6c997ce2fe4eddb`  
		Last Modified: Fri, 07 Nov 2025 00:22:34 GMT  
		Size: 128.5 MB (128469419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f19b411f4df8b6caa378110af7d17fe6173e2e120ca0f853246db23ab95376`  
		Last Modified: Thu, 06 Nov 2025 23:13:53 GMT  
		Size: 59.5 KB (59522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:75ec8f7667b9da218ba9ea4f5cccdefd9b421ad4acea9a41b6a69bf4bce23062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11248948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7ac73ecb0b06a5b9fb535bfd1a4c822a5c4327ab18f8fbb451d6aad689e5014`

```dockerfile
```

-	Layers:
	-	`sha256:8a090df1c08400296b074aafb7d429843e1be03b9c5ef54792fbaf14ca5abe4a`  
		Last Modified: Fri, 07 Nov 2025 00:18:52 GMT  
		Size: 11.2 MB (11228062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc3de41fd5a6e400da8c9f1c2efb285e1665037ee73328d82f89d5441531bfbb`  
		Last Modified: Fri, 07 Nov 2025 00:18:53 GMT  
		Size: 20.9 KB (20886 bytes)  
		MIME: application/vnd.in-toto+json
