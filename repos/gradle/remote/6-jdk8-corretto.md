## `gradle:6-jdk8-corretto`

```console
$ docker pull gradle@sha256:07e650b861a95bbd479710f836c137ab974f468755b1136085dc348e9b0de739
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk8-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:e6a6bd19eb186f9ae611a78d74396908728a08069e41e3b58a8fbffcf4bd6cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **558.5 MB (558488341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa462320b3bdb8128706317961a0a89fdeb8d796708814c9192a8f7e5c34b3`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:05:57 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 17:05:57 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:05:57 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:05:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 03 Apr 2026 17:13:50 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:13:50 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:13:50 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:13:50 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:13:50 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:13:51 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:13:51 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 03 Apr 2026 17:13:51 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 03 Apr 2026 17:13:53 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:13:53 GMT
USER gradle
# Fri, 03 Apr 2026 17:13:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 17:13:54 GMT
USER root
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81535bfa6f7dd029d87921d4ee5a42b77b0743bb69fcf1a6effada460edf0aaa`  
		Last Modified: Fri, 03 Apr 2026 17:06:51 GMT  
		Size: 330.9 MB (330930128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719cd8e8d6ece20e15861732cc1ae0e2c4d91b251b8712a390ab49464e02f3c8`  
		Last Modified: Fri, 03 Apr 2026 17:14:32 GMT  
		Size: 65.4 MB (65395199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539cd63c1334e67b59942493ce42e9f21980b28b0b11f70ab29d1a1f07cc39db`  
		Last Modified: Fri, 03 Apr 2026 17:14:29 GMT  
		Size: 1.9 KB (1941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bf466e3b90886eb0815ddc63ba9e1c93aefef9d628f8970721dec932c3a566`  
		Last Modified: Fri, 03 Apr 2026 17:14:32 GMT  
		Size: 107.7 MB (107696665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5285f5c2f65c59a97d45d5881e345141a4df83191b9f05732c60b90b4e5aaed`  
		Last Modified: Fri, 03 Apr 2026 17:14:29 GMT  
		Size: 431.3 KB (431286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b507594fcf1a385fcbd54578ed89d7d343dc982de1faaa450309f89607ee4671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18066924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f3e06cdfbde92a4a3c956c4fde72073d0752b6e205c637c5b829188c680401c`

```dockerfile
```

-	Layers:
	-	`sha256:be8ee866af685acfe4eb7189a3e13ed158005294ba306a551c6363c995b46626`  
		Last Modified: Fri, 03 Apr 2026 17:14:30 GMT  
		Size: 18.0 MB (18046059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15592f514101fdf3294b114006322b521ac22f112b04de8932d3f0bf0b7e3da1`  
		Last Modified: Fri, 03 Apr 2026 17:14:29 GMT  
		Size: 20.9 KB (20865 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk8-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:23a1a51f66acdd92ba48b9b896e744a25c3c4f69a8004c1f19ad4427beac8218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364564872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2250b2c5b468bf374c810f531bbd40b207f2c7ba36941aef38cb9594a9a15341`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:13:34 GMT
ARG version=1.8.0_482.b08-1
# Fri, 03 Apr 2026 17:13:34 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:13:34 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:13:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 03 Apr 2026 17:33:43 GMT
CMD ["gradle"]
# Fri, 03 Apr 2026 17:33:43 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 03 Apr 2026 17:33:43 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 03 Apr 2026 17:33:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 03 Apr 2026 17:33:44 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 03 Apr 2026 17:33:44 GMT
WORKDIR /home/gradle
# Fri, 03 Apr 2026 17:33:44 GMT
ENV GRADLE_VERSION=6.9.4
# Fri, 03 Apr 2026 17:33:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Fri, 03 Apr 2026 17:33:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 03 Apr 2026 17:33:46 GMT
USER gradle
# Fri, 03 Apr 2026 17:33:46 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 03 Apr 2026 17:33:46 GMT
USER root
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1aa8e5e0737da73799f0150412039fe08c46d3ce741b2162d8b0315532411c`  
		Last Modified: Fri, 03 Apr 2026 17:13:54 GMT  
		Size: 118.0 MB (117964689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a436b847f47b75768272b9626cd673ab3f0848a1a12004447011b9e3cf9fb56`  
		Last Modified: Fri, 03 Apr 2026 17:34:17 GMT  
		Size: 85.5 MB (85535439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff30758e867eef8f0f9a2a4d86168029ed57311aa3218d7ac969010b6b160a2`  
		Last Modified: Fri, 03 Apr 2026 17:34:14 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de8a4020847a97f0588d95267b0bbdd4c74bbd1be189729fc1de5d8eae3b5d0`  
		Last Modified: Fri, 03 Apr 2026 17:34:18 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61cda121d1e6274ea5aa1fb4649819814ecbbc8fda250434d02dc7aa467c766`  
		Last Modified: Fri, 03 Apr 2026 17:34:14 GMT  
		Size: 425.0 KB (425021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk8-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:44c40a32d81a0fb7104e9f566bf1c1167734729ccfc918eb01a2ac22d62e3203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11631261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97d9727c11e1b89685588c31e6f739eaa6c5b65a75f9765551ed4890c742dc8`

```dockerfile
```

-	Layers:
	-	`sha256:448487cb207133a61f82b0b286f78563c5d5cfde63ed1d91fba290cda6e05cf1`  
		Last Modified: Fri, 03 Apr 2026 17:34:14 GMT  
		Size: 11.6 MB (11610223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e62cbdc6d4fdec05d8383a780eb4c72bc8e452cb6ed36d2a66ab4b23c9acaee3`  
		Last Modified: Fri, 03 Apr 2026 17:34:14 GMT  
		Size: 21.0 KB (21038 bytes)  
		MIME: application/vnd.in-toto+json
