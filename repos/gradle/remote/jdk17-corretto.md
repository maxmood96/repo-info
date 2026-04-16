## `gradle:jdk17-corretto`

```console
$ docker pull gradle@sha256:a833aae62d638b70dd2276e72cb661012e7fb46df475ebdf0949eb6454d52c3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:ac7303dd4daae1cc6c68b3ff13d1761113d1900839d0da731af869f0143dbd03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.4 MB (435419610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6e756d6d8c71430bb95d51b5f34427268201ccc78d9b684b4c19c6f817f02b`
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
# Wed, 15 Apr 2026 22:17:37 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:17:37 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:17:37 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:17:37 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 22:17:37 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:17:37 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:17:37 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 15 Apr 2026 22:17:37 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 15 Apr 2026 22:17:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:17:40 GMT
USER gradle
# Wed, 15 Apr 2026 22:17:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 15 Apr 2026 22:17:40 GMT
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
	-	`sha256:8fa70506eba4c4dccaa87a7ffbbb78b3be1f1880d95c4d10bdf38d38b833c963`  
		Last Modified: Wed, 15 Apr 2026 22:18:10 GMT  
		Size: 86.1 MB (86101613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8110dd7d7f8945bfa37e341534c929672976f66374193a23fc3ea762bc89fd59`  
		Last Modified: Wed, 15 Apr 2026 22:18:07 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59d5bb0c38cee9a1663cd7301df5ac0319978fe242ab9631d0992fe5d4edd54`  
		Last Modified: Wed, 15 Apr 2026 22:18:12 GMT  
		Size: 137.8 MB (137808336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e665a26acc3fd248be941465a729588a2f422c6b0366bf9e2bbf0e4f42c66cea`  
		Last Modified: Wed, 15 Apr 2026 22:18:07 GMT  
		Size: 25.6 KB (25605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:3af3144ed7b3550287261c914a3b0c4eac7987071b45509d40e716d64b0a5df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11355918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdcf2a01391735131ffb0f7b158c6b6540b0496890467d19d34d0cc15be3f90`

```dockerfile
```

-	Layers:
	-	`sha256:d3ed1c60a70fa6fbeabd51a77ce81b7fd1ba506ab776eba9fa16bd7464535cea`  
		Last Modified: Wed, 15 Apr 2026 22:18:08 GMT  
		Size: 11.3 MB (11334421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18a198e44a125705ae94737629c8f24afcd941da31f22e6480026d2333ddc258`  
		Last Modified: Wed, 15 Apr 2026 22:18:07 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:7e720a973c61074b83c7e872df94a2614d25649ee9d106aaf3c433c2b3985d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.6 MB (432613434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2909882260420eb3369a6ed7ab87b21946d984245325deaf8affe37281be072d`
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
# Wed, 15 Apr 2026 22:29:58 GMT
CMD ["gradle"]
# Wed, 15 Apr 2026 22:29:58 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 15 Apr 2026 22:29:58 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 15 Apr 2026 22:29:58 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 15 Apr 2026 22:29:58 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 15 Apr 2026 22:29:58 GMT
WORKDIR /home/gradle
# Wed, 15 Apr 2026 22:29:58 GMT
ENV GRADLE_VERSION=9.4.1
# Wed, 15 Apr 2026 22:29:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
# Wed, 15 Apr 2026 22:30:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 15 Apr 2026 22:30:01 GMT
USER gradle
# Wed, 15 Apr 2026 22:30:01 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=2ab2958f2a1e51120c326cad6f385153bb11ee93b3c216c5fccebfdfbb7ec6cb
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Wed, 15 Apr 2026 22:30:01 GMT
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
	-	`sha256:1ee9955d38d73c87bec846e8bff943f146a3edce08ef220ee73460b2c6a8b905`  
		Last Modified: Wed, 15 Apr 2026 22:30:43 GMT  
		Size: 85.6 MB (85602959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e85fb9c1d1a1f3a5c02113b6ec7f9d3ff8c4a6b4a56a7cb71f460cb73b6dca3`  
		Last Modified: Wed, 15 Apr 2026 22:30:40 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4dd2237a4b3978f795189e885dfc6cc553197353ca1503584eda2b037402d10`  
		Last Modified: Wed, 15 Apr 2026 22:30:50 GMT  
		Size: 137.8 MB (137808331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738a2b62452d76afe0d6718edaaefedd0c2d9ed838131f1d31205cd0a4fd56b2`  
		Last Modified: Wed, 15 Apr 2026 22:30:40 GMT  
		Size: 29.3 KB (29323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:54f3b008a84eadb8f196b4a4bf803508233a83d5a429233c224c60bc63b9a418
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11355114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c50d48fe1fb97c5941837b7a5f9e0e1357cd0f83619498e7eeab43394ae53d`

```dockerfile
```

-	Layers:
	-	`sha256:b4677967aa9926b2e31c12911cda8d80b201c0dffba4445f00e909aa0f3e2fd3`  
		Last Modified: Wed, 15 Apr 2026 22:30:40 GMT  
		Size: 11.3 MB (11333420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d8bc16bd638734dfb6f390cd710ead8582aa1480ce3a9bd023a6919296b0bf0`  
		Last Modified: Wed, 15 Apr 2026 22:30:39 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
