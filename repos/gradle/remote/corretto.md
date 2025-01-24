## `gradle:corretto`

```console
$ docker pull gradle@sha256:7eea7bfed88d5a21f58bc14911f69ac85396db72bd3d01a79bc4ade86399ae2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:corretto` - linux; amd64

```console
$ docker pull gradle@sha256:827fe4e1f877ae64e992684bad87af819ac9e7719147a2b8e88dc1536132be77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.2 MB (430192055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8f8ac6470831d7a1e595c6a32a762bbcd3f1b6b8d8e17c1ef862ab6ab501bc`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:40 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 15:45:23 GMT
ARG version=21.0.6.7-1
# Tue, 21 Jan 2025 15:45:23 GMT
ARG package_version=1
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 21 Jan 2025 15:45:23 GMT
CMD ["gradle"]
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Jan 2025 15:45:23 GMT
WORKDIR /home/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_VERSION=8.12
# Tue, 21 Jan 2025 15:45:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
USER gradle
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
USER root
```

-	Layers:
	-	`sha256:fa97b7596fdd91f8ccf1ccf8ee7189f9449877cc795e39ad814638444b666c80`  
		Last Modified: Fri, 17 Jan 2025 02:00:45 GMT  
		Size: 53.2 MB (53152535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54526538d126c7e701e5bad2a88c117277eaf596cbbd1417cf06d8163fba3823`  
		Last Modified: Thu, 23 Jan 2025 23:08:21 GMT  
		Size: 169.8 MB (169756115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30ba431a006b13bffb377444df0576d27dc35193497688f83ba514a8c3d7722`  
		Last Modified: Fri, 24 Jan 2025 00:08:30 GMT  
		Size: 70.7 MB (70662753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222bf45b1dc720256bd5ec540e40c0a2fb04d3414d2d1fb41215d2f8148756b8`  
		Last Modified: Fri, 24 Jan 2025 00:08:29 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65192ce7c17d731ed59e3526018b88f5c44d0dfadd410a2acc3b39d98584edcf`  
		Last Modified: Fri, 24 Jan 2025 00:08:31 GMT  
		Size: 136.6 MB (136564074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b76dbca626b993ec37f39be28f66aa3bc2526dc7444dfb00ad24536f596861e`  
		Last Modified: Fri, 24 Jan 2025 00:08:29 GMT  
		Size: 54.9 KB (54901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c40fc6de7ebcf05819e991527fb5687f052f8a2531b96acb9115a4b4b8d91c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79fbf504ac869d94c483f99e8b72cbd36f76664f2d31ee46a404bf4b76be701`

```dockerfile
```

-	Layers:
	-	`sha256:5a7a6e8b57816e271bc26567395b65e378490c88b959140a65ff869bbff70f08`  
		Last Modified: Fri, 24 Jan 2025 00:08:29 GMT  
		Size: 10.7 MB (10720480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12604cef3ad53c89a0b6db9ea53d9ef5989bd0ae09343c09ba7761a8f71d8069`  
		Last Modified: Fri, 24 Jan 2025 00:08:29 GMT  
		Size: 20.5 KB (20519 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:42dbd63bff40d84a8234c6a0446ca4b8bc7430600c0d8c4a36a9ea0565d46eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.3 MB (427322232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9f9d491023f2c952ccd2a451cb3343edf10eab2b92d6b41ac867ea960c5b1b3`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:44 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 15:45:23 GMT
ARG version=21.0.6.7-1
# Tue, 21 Jan 2025 15:45:23 GMT
ARG package_version=1
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
ENV LANG=C.UTF-8
# Tue, 21 Jan 2025 15:45:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 21 Jan 2025 15:45:23 GMT
CMD ["gradle"]
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 21 Jan 2025 15:45:23 GMT
WORKDIR /home/gradle
# Tue, 21 Jan 2025 15:45:23 GMT
ENV GRADLE_VERSION=8.12
# Tue, 21 Jan 2025 15:45:23 GMT
ARG GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
USER gradle
# Tue, 21 Jan 2025 15:45:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7a00d51fb93147819aab76024feece20b6b84e420694101f276be952e08bef03
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 21 Jan 2025 15:45:23 GMT
USER root
```

-	Layers:
	-	`sha256:23c58bc83b4b2c70780808282eab12c25cdbe212cc6fa4cd0d9a4d82b1cbf7ce`  
		Last Modified: Fri, 17 Jan 2025 02:10:39 GMT  
		Size: 52.3 MB (52270199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23e56705959971e6a5303bbeaaff3bb398605ff3561b9a2abe5a5f86bd115b8`  
		Last Modified: Thu, 23 Jan 2025 23:23:38 GMT  
		Size: 168.1 MB (168064367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41b4a592cb29430191d3906d967844cd0db8c0f56cfa08eb0824bffbaf341f6`  
		Last Modified: Fri, 24 Jan 2025 00:12:06 GMT  
		Size: 70.4 MB (70362384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9926b909f18f2252595b58ff21f592de3a764e2623972cff753207db265bb865`  
		Last Modified: Fri, 24 Jan 2025 00:12:03 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01290873e85ffb5c964d77fad2344f0eff28ca9b4dc6bac84c73bcb53362b8f5`  
		Last Modified: Fri, 24 Jan 2025 00:12:08 GMT  
		Size: 136.6 MB (136564072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d28c1f7249ce5929964560f39145006129324021595b55c31989c192aede52a`  
		Last Modified: Fri, 24 Jan 2025 00:12:04 GMT  
		Size: 59.5 KB (59530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:dbd8b3fdc02f7d3daee2620dc66f3032b014eb576f4b4c92f7738c97f2a8c9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10740246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913da1dea77fd1100f8a249ee5f9f8cb1cac0ad0726f4797d74f93fe30ec1baf`

```dockerfile
```

-	Layers:
	-	`sha256:2e178eb9596ec2525c0873c2c4a165247a55f92fc2d4b5e082e70703f90ac682`  
		Last Modified: Fri, 24 Jan 2025 00:12:04 GMT  
		Size: 10.7 MB (10719506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e50768383d70e5e880af3b2490233c5d908f4a50c782970d0fc94030144fc8b`  
		Last Modified: Fri, 24 Jan 2025 00:12:03 GMT  
		Size: 20.7 KB (20740 bytes)  
		MIME: application/vnd.in-toto+json
