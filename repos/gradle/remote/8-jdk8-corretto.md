## `gradle:8-jdk8-corretto`

```console
$ docker pull gradle@sha256:9b659ba03c29ac34aff44f6851e8f3787e6039f758e2d324259f6e9fb44bcd77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:03f332993a9547aceb5c63f512bb715d5011eb9de1e64ee522120cc88937bf22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **587.7 MB (587697642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46204b95f2685713c2267102ba219fc77291d047c6bb202a4a015ab0f45d7cd9`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:17:48 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:17:48 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:17:48 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:17:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 18 Dec 2025 02:19:20 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:19:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:19:20 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:19:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:19:20 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:19:20 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:19:20 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 18 Dec 2025 02:19:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 18 Dec 2025 02:19:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:19:23 GMT
USER gradle
# Thu, 18 Dec 2025 02:19:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Dec 2025 02:19:23 GMT
USER root
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e34bac1605a4e3c5373bbcccfc49cb6f259622f2e93d19c2553d6de26db99f5`  
		Last Modified: Thu, 18 Dec 2025 01:18:53 GMT  
		Size: 330.9 MB (330887757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af1fbcecfc377798179ed88069cb8a4cb402691fa30686a3295296c62bbe491`  
		Last Modified: Thu, 18 Dec 2025 02:20:21 GMT  
		Size: 65.4 MB (65369346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c408eac517670064c042f457d8fe0b767b77fc51530ca41e6c760460ae07637`  
		Last Modified: Thu, 18 Dec 2025 02:20:15 GMT  
		Size: 1.9 KB (1943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5cede81b41e062ac97e57621bbd0e3fb445460e347c1a218f0b281b942970e`  
		Last Modified: Thu, 18 Dec 2025 02:20:39 GMT  
		Size: 137.4 MB (137395197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d2d51639111f8aa2203fb5c256b2c7ba63064a213c19766c588b80a4209a7f`  
		Last Modified: Thu, 18 Dec 2025 02:20:15 GMT  
		Size: 54.9 KB (54907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:7be617d2e756cb3130e6a124a91803b06059ef8d932493ca200216d50e9382cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18175389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e72bd37b5edd88203557010801dfdd6249f3cb89b92c16a6bcaf76c3bf68a5`

```dockerfile
```

-	Layers:
	-	`sha256:4e395742fff01d59d93b7f2486a981f84742ee52546730e5ffb6b991a45e246b`  
		Last Modified: Thu, 18 Dec 2025 03:20:13 GMT  
		Size: 18.2 MB (18153873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e60bfe281b958a9b678930278726540a97d73774d3c4a89f94d1aa069580d9`  
		Last Modified: Thu, 18 Dec 2025 03:20:14 GMT  
		Size: 21.5 KB (21516 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6ad08e969c74689cd09004747138c1d9a4cdb08e4fcb72c3067dcf54cf34c12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.8 MB (393772826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d526cc079d10afc2ec65d62c52765a0d0cb233d6049ecfa582496201ab35f72`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:25:23 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:25:23 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:25:23 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:25:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 18 Dec 2025 02:19:41 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:19:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:19:41 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:19:41 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:19:41 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:19:41 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:19:41 GMT
ENV GRADLE_VERSION=8.14.3
# Thu, 18 Dec 2025 02:19:41 GMT
ARG GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
# Thu, 18 Dec 2025 02:19:44 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:19:44 GMT
USER gradle
# Thu, 18 Dec 2025 02:19:45 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bd71102213493060956ec229d946beee57158dbd89d0e62b91bca0fa2c5f3531
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Thu, 18 Dec 2025 02:19:45 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de3320244c0c5e8689ab3369d4e7efe9e9c7b32724b174d2d0f966d353d04e2`  
		Last Modified: Thu, 18 Dec 2025 01:25:58 GMT  
		Size: 117.9 MB (117927137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8106746ab04b703b243960f4c44ebe7c33bc26cc357fae769eb8015c7ad86527`  
		Last Modified: Thu, 18 Dec 2025 02:20:29 GMT  
		Size: 85.5 MB (85515952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0416fc551c5e953e56ae1298618f7a08caa664b2e4c6aa522e65901c4b6179c1`  
		Last Modified: Thu, 18 Dec 2025 02:20:23 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450c79c60a3bc83fce760700f3d160c6ad46ecce2729c40aabff55e1010d9814`  
		Last Modified: Thu, 18 Dec 2025 02:20:18 GMT  
		Size: 137.4 MB (137395082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52745c87f09b691699ce08419af3c5af3847ced6618afa4be0d5e439593b3c0d`  
		Last Modified: Thu, 18 Dec 2025 02:20:23 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e0ec10175bdb01aeee75ba12a4460a1d657c84512579526277b83355202c65af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11739774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:354fa16cda376f98a985d24690e73a52801ef5dc0c48e4fa5bb71292e04fbe99`

```dockerfile
```

-	Layers:
	-	`sha256:97cd135fb8219541f16ac4742840926b63cc967f496146d1c251e8b8c9695a6f`  
		Last Modified: Thu, 18 Dec 2025 03:22:05 GMT  
		Size: 11.7 MB (11718061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a66e63c2aee5eac2c2328e6159c232eedc6e8e0b1cabb7035c080f29acf501e`  
		Last Modified: Thu, 18 Dec 2025 03:22:06 GMT  
		Size: 21.7 KB (21713 bytes)  
		MIME: application/vnd.in-toto+json
