## `gradle:corretto`

```console
$ docker pull gradle@sha256:1e6ee3a61fd1ee7925d71a3ea6ba154900010fb61aef0db13bcc651c38d5b68c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:corretto` - linux; amd64

```console
$ docker pull gradle@sha256:308155acd1647d9341c476be51957c9e8a6e091af967e90aaa7a51ccfbe689ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.4 MB (464358386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1025a1bf060f69186b0955d9d5899a9027a3fc42630b4c85ef0e22d7b93c9d`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:49 GMT
ARG version=25.0.1.8-1
# Fri, 31 Oct 2025 00:12:49 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:49 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:49 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:11:16 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:11:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:11:16 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:11:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Fri, 31 Oct 2025 01:11:16 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:11:16 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:11:16 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 31 Oct 2025 01:11:16 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 31 Oct 2025 01:11:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Fri, 31 Oct 2025 01:11:19 GMT
USER gradle
# Fri, 31 Oct 2025 01:11:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Fri, 31 Oct 2025 01:11:19 GMT
USER root
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cad330e08d585bcff7ce7b398a5a2dbb684e338ae4fe298f9dca43f057f4b8c`  
		Last Modified: Fri, 31 Oct 2025 01:10:53 GMT  
		Size: 189.2 MB (189165602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6348abbb214b3b9bacf61810febd5a4ebb1ed08b1d57e3eea5ae8c846b0d488`  
		Last Modified: Fri, 31 Oct 2025 01:12:22 GMT  
		Size: 85.6 MB (85613238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d894cc18ce67dd848d3eb84bec9ac459990b15ae8824984265f5bf9292dd2d`  
		Last Modified: Fri, 31 Oct 2025 01:12:06 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e98ffc381bfe8c40223e5759c2bad6e821924a149775da8071842b916dac60`  
		Last Modified: Fri, 31 Oct 2025 04:21:39 GMT  
		Size: 135.5 MB (135521732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a731fc8abe7521cd020f75be50d17dbef9ba35edd22fdec3fbc9631335279d85`  
		Last Modified: Fri, 31 Oct 2025 01:12:06 GMT  
		Size: 54.9 KB (54899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:e4d015c2d7a8e48d930200c632e230d98a4b89e023befdde9f7bb39e1638fcb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11350173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fd15b022c54507efd97d2c5e3976e2bffa36b7429de24f489cf88625c3f79e`

```dockerfile
```

-	Layers:
	-	`sha256:2e3583003e03bb21059687aee4aa49b48d7d65a951f6fcd0e5488bc4c1ff26c6`  
		Last Modified: Fri, 31 Oct 2025 02:23:50 GMT  
		Size: 11.3 MB (11327953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c235b920e61f84fffffa4a2658b7e06a3a1ed44ef116788dc106f1c6f6b7516`  
		Last Modified: Fri, 31 Oct 2025 02:23:51 GMT  
		Size: 22.2 KB (22220 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:6e24df6fea02007e13763ebd3ef3d8f0ee049911e5e17c3c27b609db63e27ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.7 MB (460742863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40d9beb67d4f303dff7276d7a1c852e376481414ebca02913224f296fc11036`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:16:48 GMT
ARG version=25.0.1.9-1
# Tue, 04 Nov 2025 23:16:48 GMT
ARG package_version=1
# Tue, 04 Nov 2025 23:16:48 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Nov 2025 23:16:48 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 04 Nov 2025 23:25:56 GMT
CMD ["gradle"]
# Tue, 04 Nov 2025 23:25:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Nov 2025 23:25:56 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Nov 2025 23:25:56 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 04 Nov 2025 23:25:56 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Nov 2025 23:25:56 GMT
WORKDIR /home/gradle
# Tue, 04 Nov 2025 23:25:56 GMT
ENV GRADLE_VERSION=9.2.0
# Tue, 04 Nov 2025 23:25:56 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Tue, 04 Nov 2025 23:25:59 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 04 Nov 2025 23:25:59 GMT
USER gradle
# Tue, 04 Nov 2025 23:26:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Tue, 04 Nov 2025 23:26:00 GMT
USER root
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9365c25afe64e4be1bd920de12cba12a4866ebadce41ee02775bebe9869913ec`  
		Last Modified: Tue, 04 Nov 2025 23:25:30 GMT  
		Size: 187.1 MB (187092250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2413124ec7000087d2978bdca6145f156854e952594f16fcab04c549bc5b2acb`  
		Last Modified: Tue, 04 Nov 2025 23:26:54 GMT  
		Size: 85.2 MB (85165891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545be04cc6e5db5880e5fbbdab7385a616bf4a86baa6206d3b519f19f6443e7a`  
		Last Modified: Tue, 04 Nov 2025 23:26:48 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b263bcfee48fdbd35bc918f83fdd0a66bff1ac4698382d34562f3b62dbd6fe`  
		Last Modified: Tue, 04 Nov 2025 23:26:33 GMT  
		Size: 135.5 MB (135521663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5b642fc7aabb338656a47b2681f0f298de30ecb97428733987cbd69cce98e7`  
		Last Modified: Tue, 04 Nov 2025 23:26:45 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:66a648ddfb983691f8c69e7747c27dadb35d2a3db41eb85fa5ad30ed52b85325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11349431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ca99236c76c6866b4126ed48386f15cc1f1bdac9106bd3c0867bca3fe6edfe7`

```dockerfile
```

-	Layers:
	-	`sha256:9fb74634612cf0b9bcd79c1f1de653c3fa88217da7e5c96e4bf10d26d45be77e`  
		Last Modified: Wed, 05 Nov 2025 00:21:42 GMT  
		Size: 11.3 MB (11326990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbe9cb9c67e14d4244e0bc14b9ab64bdfee2a64d7d1c344097021d4410814216`  
		Last Modified: Wed, 05 Nov 2025 00:21:43 GMT  
		Size: 22.4 KB (22441 bytes)  
		MIME: application/vnd.in-toto+json
