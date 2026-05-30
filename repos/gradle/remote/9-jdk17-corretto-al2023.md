## `gradle:9-jdk17-corretto-al2023`

```console
$ docker pull gradle@sha256:5213a15e8b40fe0b3f0ce3058f0f6af0d8be609aced4c7838026a6e147a011be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk17-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:fc3c7fb9533aefdf3a53bc99026f2cd2423787e96d8cdb04d67de650d7b7dea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.3 MB (438256648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6eaf596b9a408cc6f5c49ff373201a64f78de328156c721a01c0eba2feb7d2`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:59 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:59 GMT
ARG package_version=1
# Sat, 30 May 2026 01:11:59 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:59 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 30 May 2026 02:11:29 GMT
CMD ["gradle"]
# Sat, 30 May 2026 02:11:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 May 2026 02:11:29 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 30 May 2026 02:11:29 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 30 May 2026 02:11:29 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 May 2026 02:11:29 GMT
WORKDIR /home/gradle
# Sat, 30 May 2026 02:11:29 GMT
ENV GRADLE_VERSION=9.5.1
# Sat, 30 May 2026 02:11:29 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Sat, 30 May 2026 02:11:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:11:32 GMT
USER gradle
# Sat, 30 May 2026 02:11:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 30 May 2026 02:11:33 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f5461596ec82cf1472eb49d2c4ccb688b3d1a9f53b7f3ed65132c7161de215`  
		Last Modified: Sat, 30 May 2026 01:12:20 GMT  
		Size: 157.2 MB (157156699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7ba808f285fd4aa0c5266d69a6fe8d110483a008752e3c8c4c049ebb26ecab`  
		Last Modified: Sat, 30 May 2026 02:12:03 GMT  
		Size: 86.3 MB (86264527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edbfd72097465bed054ed57035cf53cbba5136b27754751fceffbb4558494c5`  
		Last Modified: Sat, 30 May 2026 02:11:59 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401c00250cea11d0f5913ca703b432f13fa1500b94f9b2df43968242c85b8f42`  
		Last Modified: Sat, 30 May 2026 02:12:05 GMT  
		Size: 140.2 MB (140236980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a926fd5ba2fdd118046f3e1d24d56c927223da9ffb0b1ff643ef1b1fed261d3`  
		Last Modified: Sat, 30 May 2026 02:12:00 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:d4485d2d697134df9a73da2177eae7a8e811012c379533b55bfbf021e5649e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11319d3ef2863b84477b8fe5f6ef2fb9ca1e8df93babcd55a75ef585b595440`

```dockerfile
```

-	Layers:
	-	`sha256:fc2514f2fb08ef9182d0904f3633e3b90827e97477987685dc6f29a012ab1fb5`  
		Last Modified: Sat, 30 May 2026 02:12:00 GMT  
		Size: 11.4 MB (11365662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c23dd494bb0704928cacc6da406a72bc847a50f143f1165d77f0813933a9f5eb`  
		Last Modified: Sat, 30 May 2026 02:12:00 GMT  
		Size: 21.5 KB (21497 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk17-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c2fb417706401527ec1c7d045180b69949f8719d70df851ebfdbcdfa3434c1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.4 MB (435434505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cbbfc227255c2ec4042b8ca8be736db526deec23f3667df5b4a3c60fd6d5cd`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:35 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:11:35 GMT
ARG package_version=1
# Sat, 30 May 2026 01:11:35 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:35 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sat, 30 May 2026 02:11:32 GMT
CMD ["gradle"]
# Sat, 30 May 2026 02:11:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 May 2026 02:11:32 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 30 May 2026 02:11:33 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 30 May 2026 02:11:33 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 May 2026 02:11:33 GMT
WORKDIR /home/gradle
# Sat, 30 May 2026 02:11:33 GMT
ENV GRADLE_VERSION=9.5.1
# Sat, 30 May 2026 02:11:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Sat, 30 May 2026 02:11:35 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:11:35 GMT
USER gradle
# Sat, 30 May 2026 02:11:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 30 May 2026 02:11:36 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9482a7eeb42d8af7aec6211eea7980986e31da05224bb8f4570edda7f0275cdf`  
		Last Modified: Sat, 30 May 2026 01:11:58 GMT  
		Size: 156.0 MB (155987199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec292dea4a0117fc6a9c2c2a80013805c389c2d8fe88af8533ff3fb6085160d`  
		Last Modified: Sat, 30 May 2026 02:12:07 GMT  
		Size: 85.7 MB (85721495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7102051fee1e834b0428a2ae0e5d860658643152913b916430a58ce7e9c86f5`  
		Last Modified: Sat, 30 May 2026 02:12:04 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b93c4e6b3a8c6d749b1f2d4706e901a2871509c0c66693e5009547aa6aa3c9`  
		Last Modified: Sat, 30 May 2026 02:12:09 GMT  
		Size: 140.2 MB (140236982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab88bc7685efb81e88d2a61080ac9ad9edf33c84a78020077e2d0ff0c9ec5f2`  
		Last Modified: Sat, 30 May 2026 02:12:04 GMT  
		Size: 29.3 KB (29325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk17-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:fb189b5bb60a2fa839a5f975f9eca7a18405879005d2ec6731825933cb78bc43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11386356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357c139187bb76ca20859025037c97648b56dc95b09d4d03afce781a98a2a038`

```dockerfile
```

-	Layers:
	-	`sha256:cb470d5bf742153f86454740793ab1125f93b6cf59db18be6c21be92b9b1420f`  
		Last Modified: Sat, 30 May 2026 02:12:05 GMT  
		Size: 11.4 MB (11364662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb6967b91ff280a7fbbbd67448f38d543c7622ec481a1e81453238752872d70`  
		Last Modified: Sat, 30 May 2026 02:12:04 GMT  
		Size: 21.7 KB (21694 bytes)  
		MIME: application/vnd.in-toto+json
