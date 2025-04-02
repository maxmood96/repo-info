## `gradle:7-jdk17-corretto`

```console
$ docker pull gradle@sha256:01279bcab4ac41cb2c7c55399db6d696ef29b700721ce59b84407bd84cb1422a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk17-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:bc438fe42b26e453705d9c1a2acbec58c43b1c3f1df6fae043167a243205b8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.8 MB (405830731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d11288b1f49a9be91dbe60bde394b0ca603a91f91ab1743bd3590460cb0a7b`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcbc652f7f80f0a3735283bc08cab443e34a0784c311e1ebaf20079af1ef47a`  
		Last Modified: Wed, 02 Apr 2025 00:00:36 GMT  
		Size: 156.6 MB (156631936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0619eec034802f797fed9f0351f1537babaa2d8e93cc0471f35cffd332dd431`  
		Last Modified: Wed, 02 Apr 2025 00:08:28 GMT  
		Size: 70.5 MB (70504637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1641a641bb28422dd7d872fde808545c77eafc22791ac5e1cf8e51f852f517d`  
		Last Modified: Wed, 02 Apr 2025 00:08:27 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5af089abfe21c52422ad7d4914db5488d1a2c3696cee3194116ccadbe61092`  
		Last Modified: Wed, 02 Apr 2025 00:08:29 GMT  
		Size: 122.7 MB (122730528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1e4f4d7c338a213cb94787dbb3a51f0e978f434b7e7a2341dff239e57f834a`  
		Last Modified: Wed, 02 Apr 2025 00:08:27 GMT  
		Size: 54.9 KB (54900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:c72b694668b184598db147fa90bdee55f09a2c13f688c46339a18f94e25d4c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10674805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce5fbe280827c2cda673ba890e9a491b17fa0ee22f0a49bd08853dfbe88c08`

```dockerfile
```

-	Layers:
	-	`sha256:84dadcdf5a26327b32ca56e4f790aced447f7493fd9496985343c721c7835f94`  
		Last Modified: Wed, 02 Apr 2025 00:08:27 GMT  
		Size: 10.7 MB (10655706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2acfa204001ed4e7efc2023e134dc66c4382c011d024e6ac096b13bafa543ad7`  
		Last Modified: Wed, 02 Apr 2025 00:08:27 GMT  
		Size: 19.1 KB (19099 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk17-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:c9ec2eaddede82c50a95936767452e8bbb04acf708b909c595ff85ffd63dae79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.2 MB (403209495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f9f1ab4f9747addb35ccad04682fddab194b3bb0465ffa4fba0001f4264328`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Sun, 30 Mar 2025 18:23:11 GMT
CMD ["gradle"]
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
VOLUME [/home/gradle/.gradle]
# Sun, 30 Mar 2025 18:23:11 GMT
WORKDIR /home/gradle
# Sun, 30 Mar 2025 18:23:11 GMT
ENV GRADLE_VERSION=7.6.4
# Sun, 30 Mar 2025 18:23:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER gradle
# Sun, 30 Mar 2025 18:23:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sun, 30 Mar 2025 18:23:11 GMT
USER root
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b7d714897995a41856e471f38922dcd19aaa5a05568bd7114b2f60f0089ffa`  
		Last Modified: Wed, 02 Apr 2025 00:30:52 GMT  
		Size: 155.5 MB (155484238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab05ca1899a3cce961d930066dbc987ad23fa27515a118f3e39ff5f59e607f6`  
		Last Modified: Wed, 02 Apr 2025 01:09:19 GMT  
		Size: 70.0 MB (69972518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b46792a18acdefee99a2391deeff54d2da96a09401c8cf80e0a1315bbe20074`  
		Last Modified: Wed, 02 Apr 2025 01:09:17 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa449cb5d58cbfe2d7f04a5e1777e5684f4835da3899be9f35d69f023161c8e7`  
		Last Modified: Wed, 02 Apr 2025 01:12:07 GMT  
		Size: 122.7 MB (122730528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6163065aadf2c5336d7736e82653315c2935cf2ce424cddd93032da712e71264`  
		Last Modified: Wed, 02 Apr 2025 01:12:04 GMT  
		Size: 59.5 KB (59526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk17-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bef22fa1a06eb0e230a1e2ef3404ae2e460e0746ad4f053ff31679bbf2b1ecee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10673957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2509e494caa828e79ea8e533c0f1a0c1f9d6d1017e4decc959bbf4c8d9e74d6c`

```dockerfile
```

-	Layers:
	-	`sha256:4b4bbd9e7d6de8bd9622c651c3e046bc87a382515e669cb4f6ae13a5217fd6b9`  
		Last Modified: Wed, 02 Apr 2025 01:12:04 GMT  
		Size: 10.7 MB (10654685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6daf8b6c062f1c86ad99ee3fb4b2c93b6f5ac94f5aa50ac934dd1db03d20354`  
		Last Modified: Wed, 02 Apr 2025 01:12:03 GMT  
		Size: 19.3 KB (19272 bytes)  
		MIME: application/vnd.in-toto+json
