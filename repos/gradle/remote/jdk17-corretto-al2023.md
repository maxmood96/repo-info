## `gradle:jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:97bdffd7dbc471caa018ebe0a668cf5273ba2d3044a3e1ce876fdcddc414efe3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:fd1bb6f74e9e92c549ffb328606aeb3999d90a23b351ab135713ccd5bc8b839f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.5 MB (432486078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9924d2931ce37600f9743175b75f11cce878d1d06a04d747f6616e4aedecb26`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:18:03 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:18:03 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:18:03 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:18:03 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 18 Dec 2025 02:18:49 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:18:49 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:18:49 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:18:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:18:50 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:18:50 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:18:50 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 18 Dec 2025 02:18:50 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 18 Dec 2025 02:18:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:18:52 GMT
USER gradle
# Thu, 18 Dec 2025 02:18:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 18 Dec 2025 02:18:52 GMT
USER root
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c94f0e66ab1ff3543f3fe4f588fab226e2b88a2253456fb47f3f5070963e3f`  
		Last Modified: Thu, 18 Dec 2025 01:18:57 GMT  
		Size: 156.9 MB (156900599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c669cfda19e8abf978dfb4013abcf398bcc01b650020f53e47dd3f8cb42b4b54`  
		Last Modified: Thu, 18 Dec 2025 02:19:38 GMT  
		Size: 86.0 MB (86018479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69790b8353620ca14847a30d75bcfb4eb270a6eb3da343043b25629874f0749a`  
		Last Modified: Thu, 18 Dec 2025 02:19:30 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99df4ba6d0ac73f4999aff0a7771a5e2c792b954e157a48267552919b209deff`  
		Last Modified: Thu, 18 Dec 2025 02:19:59 GMT  
		Size: 135.5 MB (135521965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92faf178abd8182105b71cfee6b40880405369755341c32723736ef1ae2b7920`  
		Last Modified: Thu, 18 Dec 2025 02:19:30 GMT  
		Size: 54.9 KB (54890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:9250e12de9522aab41e3394ace7b7fcc7cec4f7fca6d0970d0d984832d95d357
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11356239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e73a39536577790f2576c7593ccd90d719f836a66d80d39608442d6f34d80e7`

```dockerfile
```

-	Layers:
	-	`sha256:07f0cf525133a7ba378ca84abdecec3f372765857c01bbe0b259f1a7bba98edd`  
		Last Modified: Thu, 18 Dec 2025 03:22:35 GMT  
		Size: 11.3 MB (11334742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1195c7abe20bdddcb2d9e8f299189369284da0bc04a41062b6588d2f21632b92`  
		Last Modified: Thu, 18 Dec 2025 03:22:36 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:4658d6dc0e23bc0f2670b587d597601736659f6c32b001ad7aa6036a4fe614e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.7 MB (429686484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d2d62d42b07bb6a93c1b435304abdf607e7b8aed94530f29a40b4b17ee17dd`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:26:29 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:26:29 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:26:29 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:26:29 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 18 Dec 2025 02:19:12 GMT
CMD ["gradle"]
# Thu, 18 Dec 2025 02:19:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Dec 2025 02:19:12 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 18 Dec 2025 02:19:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Thu, 18 Dec 2025 02:19:13 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Dec 2025 02:19:13 GMT
WORKDIR /home/gradle
# Thu, 18 Dec 2025 02:19:13 GMT
ENV GRADLE_VERSION=9.2.1
# Thu, 18 Dec 2025 02:19:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
# Thu, 18 Dec 2025 02:19:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Thu, 18 Dec 2025 02:19:15 GMT
USER gradle
# Thu, 18 Dec 2025 02:19:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=72f44c9f8ebcb1af43838f45ee5c4aa9c5444898b3468ab3f4af7b6076c5bc3f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Thu, 18 Dec 2025 02:19:16 GMT
USER root
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f9dca445f419513819266ddecf7477b069aa5b3d4e331702639766d5ce2a1`  
		Last Modified: Thu, 18 Dec 2025 01:27:19 GMT  
		Size: 155.7 MB (155707401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8feaeb2bbca403e11b973b0e6ba69877e86e7f54c026e56670859717a0fe96e1`  
		Last Modified: Thu, 18 Dec 2025 02:20:01 GMT  
		Size: 85.5 MB (85522465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb2670394fac4ed628afeb5828f580dda45cdd5163fa67612a9ce951e744052`  
		Last Modified: Thu, 18 Dec 2025 02:19:54 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdb5279fa3a83de7ea1c5791eeed6ad14c431cf939393641c53590d6d899791`  
		Last Modified: Thu, 18 Dec 2025 02:19:49 GMT  
		Size: 135.5 MB (135521966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3769b03b8e19ddad917ce129bcbb2b33e597eb7aca1d71834c147dd87c973f6e`  
		Last Modified: Thu, 18 Dec 2025 02:19:54 GMT  
		Size: 59.5 KB (59525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:1aafd0ec3da08afd1a6ae558eb5bbb0496b90007063f3da0d0208156486570b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11355435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25074fc9ba07accb7d3be9f84f2d6bf2d090df1d49a9d2037ede50f61d46d0e5`

```dockerfile
```

-	Layers:
	-	`sha256:0e67eeb1c7402bc8b9415d65395b2f836a8e9d8b76a2a88fd264906536abcdde`  
		Last Modified: Thu, 18 Dec 2025 03:22:45 GMT  
		Size: 11.3 MB (11333741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46422b1fd9830e7b3f67a5970988bef9694ab57ccc7ef1b8314fb251688f5cf5`  
		Last Modified: Thu, 18 Dec 2025 03:22:46 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
