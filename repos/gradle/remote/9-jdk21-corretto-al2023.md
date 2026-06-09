## `gradle:9-jdk21-corretto-al2023`

```console
$ docker pull gradle@sha256:85ec95e2ed9eda68cd1192e3349e8b5bb640de96c4cf823b4a8fa9538f430688
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:3912fef916ae8cda401e2b83e30eeaf239a0bc3ad7f4c42c574251ab0cdd5cb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451545173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c4807aa8ddbbfa57614ec9c2ac1ae1a195412fe9a17e5f26f576196d6c1392f`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:31 GMT
ARG version=21.0.11.10-1
# Tue, 09 Jun 2026 21:12:31 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:31 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:31 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 09 Jun 2026 22:05:13 GMT
CMD ["gradle"]
# Tue, 09 Jun 2026 22:05:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 09 Jun 2026 22:05:13 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 09 Jun 2026 22:05:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 09 Jun 2026 22:05:13 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 09 Jun 2026 22:05:13 GMT
WORKDIR /home/gradle
# Tue, 09 Jun 2026 22:05:13 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 09 Jun 2026 22:05:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 09 Jun 2026 22:05:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 09 Jun 2026 22:05:15 GMT
USER gradle
# Tue, 09 Jun 2026 22:05:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 09 Jun 2026 22:05:16 GMT
USER root
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655da4f67bbe8b448c113c5608d6d6a794180419e8ce9d70d44ad817230d8f55`  
		Last Modified: Tue, 09 Jun 2026 21:12:55 GMT  
		Size: 170.4 MB (170445528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71872a330c6997f2238bf5bbb5f8c3f2c2c1fb534b751237532416c4372f840`  
		Last Modified: Tue, 09 Jun 2026 22:05:46 GMT  
		Size: 86.3 MB (86264217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05923e868c11962744c2c528820347f5552b9b8ba0e43a3865949a8634e17d9`  
		Last Modified: Tue, 09 Jun 2026 22:05:42 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c500acbdcc049773514f60bbb190dc0c3e81b0c377751ecf1983cba49c5f349`  
		Last Modified: Tue, 09 Jun 2026 22:05:48 GMT  
		Size: 140.2 MB (140236983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b528a4412adfbb5eb0c822da9acc977b632f0c0a5e02f002a29d697d474b01`  
		Last Modified: Tue, 09 Jun 2026 22:05:42 GMT  
		Size: 25.6 KB (25611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:17ee3d03d199813d13df5160fb8d26bff97c3d10a6e61643967af389664a66a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11389738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39e0ef747e7208a13e6d7c1ab4ada90d28bc4a2a8fcc490efdf4e5e19261819`

```dockerfile
```

-	Layers:
	-	`sha256:8d268e7f18df325f49c16adc3be2d6cf86a0f3fffe34254e18abdde3dd9172d2`  
		Last Modified: Tue, 09 Jun 2026 22:05:43 GMT  
		Size: 11.4 MB (11368088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73b955f0acc4d1314a7ca6e4866ac3057be8969ceb3920a0163cbebc6a5b6f55`  
		Last Modified: Tue, 09 Jun 2026 22:05:42 GMT  
		Size: 21.6 KB (21650 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9a2222134bb04c12a01cad4f198b986714e3b0bbaaff147d1a79a815b0cbb33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.2 MB (448170172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb8a0ee6e4bee19228c8bccb8497dde9573a11f43118a15d85edaf726ebe256`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:28 GMT
ARG version=21.0.11.10-1
# Sat, 30 May 2026 01:12:28 GMT
ARG package_version=1
# Sat, 30 May 2026 01:12:28 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:12:28 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 30 May 2026 02:11:13 GMT
CMD ["gradle"]
# Sat, 30 May 2026 02:11:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 30 May 2026 02:11:13 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 30 May 2026 02:11:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sat, 30 May 2026 02:11:13 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 30 May 2026 02:11:13 GMT
WORKDIR /home/gradle
# Sat, 30 May 2026 02:11:13 GMT
ENV GRADLE_VERSION=9.5.1
# Sat, 30 May 2026 02:11:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Sat, 30 May 2026 02:11:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 30 May 2026 02:11:16 GMT
USER gradle
# Sat, 30 May 2026 02:11:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Sat, 30 May 2026 02:11:17 GMT
USER root
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae6dcf128c8239e095d4cadda037b6a5b5c267ad60f46b5b8fa317ff773db55`  
		Last Modified: Sat, 30 May 2026 01:12:53 GMT  
		Size: 168.7 MB (168720905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547366a0cd2b7f5c6508b7dc90aa7fc0c67b546605f0d46999ea0e31065b3ad1`  
		Last Modified: Sat, 30 May 2026 02:11:49 GMT  
		Size: 85.7 MB (85723444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4bce404339a8b53dee72b3de4b96f8befc1990d980a5e7a8142681396b5007`  
		Last Modified: Sat, 30 May 2026 02:11:45 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ba20938ee6dde5612450a687a2c67f44887097b486b6ec782e3759a38fc261`  
		Last Modified: Sat, 30 May 2026 02:11:50 GMT  
		Size: 140.2 MB (140236981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad0355ba4aa424443d71c711375e4f387552550a18455f0b4af8cc795fd5fbd`  
		Last Modified: Sat, 30 May 2026 02:11:45 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:5734f3978df5c3baabbc739a4694f97d961632f1682ff99ba25721288e83fdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11388939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefe879f9f0d09377d8293a60491419e4b35de60cd8f20d5715bd1e2d6c9843e`

```dockerfile
```

-	Layers:
	-	`sha256:fa85e73153b387312dc91df03ace1ebf95f7562dd53ccf0c17ffb57a4af75dd8`  
		Last Modified: Sat, 30 May 2026 02:11:46 GMT  
		Size: 11.4 MB (11367091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:964b58173a5fe1631c90b235e9e943418e2a0d15548c98078e61e01f2a691d28`  
		Last Modified: Sat, 30 May 2026 02:11:45 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
