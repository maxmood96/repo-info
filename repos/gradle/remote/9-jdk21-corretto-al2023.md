## `gradle:9-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:79a22da48d415c54614e3e6fb8c4c73e98c4e7b3e2c85c705871628bd7978917
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:bb0a34e923f967724be056a551f263c7e05e46eaa84c945e232e46bec3307e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451451815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78232558d41baefd851c39a2f4a198f3071ee3f312e975f59c42a7705cae151f`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:18:52 GMT
ARG version=21.0.11.10-1
# Sat, 09 May 2026 00:18:52 GMT
ARG package_version=1
# Sat, 09 May 2026 00:18:52 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:18:52 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:18:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 09 May 2026 01:20:13 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:20:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:20:13 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:20:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:20:13 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:20:13 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:20:13 GMT
ENV GRADLE_VERSION=9.5.0
# Sat, 09 May 2026 01:20:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Sat, 09 May 2026 01:20:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:20:16 GMT
USER gradle
# Sat, 09 May 2026 01:20:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:20:17 GMT
USER root
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d605a7f04b26773a6a7aba7b0d6aa1461c92ae1a610eaf0612445f5621b9a7`  
		Last Modified: Sat, 09 May 2026 00:19:14 GMT  
		Size: 170.4 MB (170444573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2ff2a693f289f8d265aa048b07e6b00487d082902381d51953f864a3d8096f`  
		Last Modified: Sat, 09 May 2026 01:20:46 GMT  
		Size: 86.2 MB (86167211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b4888243f16bfb50a485991119c65d4b62142755908b6a8881ad334d906840`  
		Last Modified: Sat, 09 May 2026 01:20:42 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a66d18ddf5a7ecc44884b0a14b49b6eb797446f42523c88402728d6c16eefb0`  
		Last Modified: Sat, 09 May 2026 01:20:48 GMT  
		Size: 140.2 MB (140235930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa24d90496a36ccb408ac9780e9a2c9471c6f5f7cf91e6c73485576eb2c824f`  
		Last Modified: Sat, 09 May 2026 01:20:43 GMT  
		Size: 25.6 KB (25617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:6480554a86c05b727f601a97e18d74ff6d0838ae021d90c45b5ac6781f35ce8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11389736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28047cd4ea38c500c334369f328ecd7378ad9c6cc5ad8c9c129a99b72dcbeabe`

```dockerfile
```

-	Layers:
	-	`sha256:077a2e75815de2e842cd08d8f3e34c25159f2e4ba43b1ad8df0516a504c2731d`  
		Last Modified: Sat, 09 May 2026 01:20:43 GMT  
		Size: 11.4 MB (11368086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd37af2cedc133c61fe9d0c4b8d37d3a14d60ebd71d5f6ffea3174a9c63d5fc5`  
		Last Modified: Sat, 09 May 2026 01:20:42 GMT  
		Size: 21.6 KB (21650 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:8424b9de69f53ea0d9e842711d748b46e337f25d4aa8d970315e46131c3be875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.1 MB (448103472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eda5341a3656f9e1634b3ce17977dbb9b1fc8ba658b0fc5ade0413e0a9ab20f`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:30 GMT
ARG version=21.0.11.10-1
# Sat, 09 May 2026 00:16:30 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:30 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:30 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 09 May 2026 01:45:36 GMT
CMD ["gradle"]
# Sat, 09 May 2026 01:45:36 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 09 May 2026 01:45:36 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 09 May 2026 01:45:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 09 May 2026 01:45:36 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 09 May 2026 01:45:36 GMT
WORKDIR /home/gradle
# Sat, 09 May 2026 01:45:36 GMT
ENV GRADLE_VERSION=9.5.0
# Sat, 09 May 2026 01:45:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
# Sat, 09 May 2026 01:45:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 09 May 2026 01:45:39 GMT
USER gradle
# Sat, 09 May 2026 01:45:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=553c78f50dafcd54d65b9a444649057857469edf836431389695608536d6b746
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 09 May 2026 01:45:40 GMT
USER root
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2600f4d09077112d700e69b97b0ce85fa53a45cf0380a0447ccdcb015a271808`  
		Last Modified: Sat, 09 May 2026 00:16:53 GMT  
		Size: 168.7 MB (168722339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3623b8a4d7e6ca145ec80e133823c9d2e2da20c5e9d6ee48ddc03454f91790ce`  
		Last Modified: Sat, 09 May 2026 01:46:12 GMT  
		Size: 85.7 MB (85657195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0395e7ad166ff79769b7052fd463895e20f4e15fdd136faf0518eba8eab4c3`  
		Last Modified: Sat, 09 May 2026 01:46:07 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f69613ebba9b129e48f00c920c8544294c72fefa556669dbac0c50ee14d899e`  
		Last Modified: Sat, 09 May 2026 01:46:14 GMT  
		Size: 140.2 MB (140235937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555a87db18b709a4e6ed71346d86c0201af89473cfa50b137cf0fd6a70d85f0b`  
		Last Modified: Sat, 09 May 2026 01:46:07 GMT  
		Size: 29.3 KB (29348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:ca5498f7ecdb74bea6c16d78287a69fd5fbb842c55d10fe566a14f7bbac7a2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11388937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f8f131bf91aeb9d98033c650a9694547473704d7279c6f061ada7a30fba732`

```dockerfile
```

-	Layers:
	-	`sha256:b38f7396c89b95c0b82a86b20f8e17b4a9be090639d8438fa00063d6b3a1bca5`  
		Last Modified: Sat, 09 May 2026 01:46:08 GMT  
		Size: 11.4 MB (11367089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc0f5121935f983738e56ca586a8084e42dabe6fdc4e0ac1d0d289e504873b97`  
		Last Modified: Sat, 09 May 2026 01:46:07 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
