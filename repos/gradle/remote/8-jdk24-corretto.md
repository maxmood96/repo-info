## `gradle:8-jdk24-corretto`

```console
$ docker pull gradle@sha256:76f5d345f24f155f1c0a8304f82337758351e62006dab2080f4700ccfe70226c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk24-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:9c21d3db7081f5345a23bcc5fcc1aaa86e2ce0fe8ecb69c2f321a394c82bb36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.2 MB (464227232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff695ce56b8783d01822acc68f4a0ca2c2b5d445b964e6b727dc2fddceed61c`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ARG version=24.0.2.12-1
# Thu, 17 Jul 2025 03:50:10 GMT
ARG package_version=1
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=C.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER gradle
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER root
```

-	Layers:
	-	`sha256:b9bd06b1e98f2884554d02055b944634294fa4d6f341ec4d0d7349c492676b31`  
		Last Modified: Sat, 09 Aug 2025 04:12:21 GMT  
		Size: 53.8 MB (53837959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d48750dcbc88918e08cdc4bda3900bf3a452f14a5f37b204bc3502dfaab038`  
		Last Modified: Wed, 13 Aug 2025 23:11:05 GMT  
		Size: 187.4 MB (187386721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10e5f26e614686296c620355a2f6716af87b08cc0c74331d474d8aa77f725c2`  
		Last Modified: Wed, 13 Aug 2025 23:12:42 GMT  
		Size: 85.6 MB (85550772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d76823d44c41490666d744366b07ea118a06b18eb090270614380e3035e957`  
		Last Modified: Wed, 13 Aug 2025 23:12:39 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bd19ae39e61c0dbf41a18c6910072650a85e11ce5f14b8093bb11dc17a6c05`  
		Last Modified: Thu, 14 Aug 2025 06:56:48 GMT  
		Size: 137.4 MB (137395196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72239c5d0c95f3003bbb25ac8209cf0ff6a8644521a91b1171515c15ef90eed2`  
		Last Modified: Wed, 13 Aug 2025 23:12:39 GMT  
		Size: 54.9 KB (54904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b56c7aecdfe1c74d2703c43933083160dc7b3071b7e133018bf0cae6781bfcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11346424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd0293a159a91f2037b1690b65868fca407e79e1be15ed52f44a9351569b500`

```dockerfile
```

-	Layers:
	-	`sha256:0ac45c97eb041042c60d32178b62a5d4c08137f9ba5b63a615b06e5aed0aada4`  
		Last Modified: Thu, 14 Aug 2025 02:21:51 GMT  
		Size: 11.3 MB (11325484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:741346def4abe76cb6fb07770033dbcb6299e3041c9e4daa28d37f4efe017eec`  
		Last Modified: Thu, 14 Aug 2025 02:21:52 GMT  
		Size: 20.9 KB (20940 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk24-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:48de52118132c87d9c42d8660a5cc50758021e4071b70d7522b4b4533c6bda82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.7 MB (460685556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be599429f75df79a78a38a3c4fc2b99bb4c2ba83c1968cecc681442287191af`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 17 Jul 2025 03:50:10 GMT
COPY /rootfs/ / # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["/bin/bash"]
# Thu, 17 Jul 2025 03:50:10 GMT
ARG version=24.0.2.12-1
# Thu, 17 Jul 2025 03:50:10 GMT
ARG package_version=1
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
ENV LANG=C.UTF-8
# Thu, 17 Jul 2025 03:50:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 17 Jul 2025 03:50:10 GMT
CMD ["gradle"]
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 17 Jul 2025 03:50:10 GMT
WORKDIR /home/gradle
# Thu, 17 Jul 2025 03:50:10 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 17 Jul 2025 03:50:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER gradle
# Thu, 17 Jul 2025 03:50:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 17 Jul 2025 03:50:10 GMT
USER root
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8fe3dd6a3466db38a1fbed83ebaa82aec0d67c18d03baa73602aa3563e2ac9`  
		Last Modified: Thu, 14 Aug 2025 12:48:43 GMT  
		Size: 185.4 MB (185426437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa7546bac13d29c07f148bdd52649ff21540722d03aa8c3191d17b3081b0100`  
		Last Modified: Thu, 14 Aug 2025 19:39:12 GMT  
		Size: 85.1 MB (85076345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10ce3982591dd9f9aed4310057b0d96ff20d2d3bdc2b8d77097877704898132`  
		Last Modified: Thu, 14 Aug 2025 19:39:02 GMT  
		Size: 1.6 KB (1642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f26d1c7d3355f85e831aceceaf800c0a664da092903b83a7de9f4a9d8a4f94`  
		Last Modified: Thu, 14 Aug 2025 19:38:29 GMT  
		Size: 137.4 MB (137395174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877bd1ba361e3f1e12928b85272bc58e03d9a4b10794da19d03dc573e63451e4`  
		Last Modified: Thu, 14 Aug 2025 19:39:02 GMT  
		Size: 59.5 KB (59532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:618b38ce2d370926f1265f2fe16936eb786e90fa855952da01084fabc8404ff3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11345570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:096dabbed3a1ad7fe3cdb1699f876e8071d3b6ca217eab7af552d5a320b093d7`

```dockerfile
```

-	Layers:
	-	`sha256:24cbb360dcd512b1fca846f560253aac5d1f904f77e4621e2362970572723983`  
		Last Modified: Thu, 14 Aug 2025 20:21:37 GMT  
		Size: 11.3 MB (11324473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e64bc9ec58c92db94027f3c985a01c97ff0fb18a1a84ebc6cc53d440e9410ea`  
		Last Modified: Thu, 14 Aug 2025 20:21:39 GMT  
		Size: 21.1 KB (21097 bytes)  
		MIME: application/vnd.in-toto+json
