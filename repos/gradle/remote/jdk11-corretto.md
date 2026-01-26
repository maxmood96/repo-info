## `gradle:jdk11-corretto`

```console
$ docker pull gradle@sha256:ba25e3f942272105d3f37a6e9e1b53b18a32af1594ffa880ec17cac0b4070971
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:1c53379e909af802bd40df24f961753447f8db09e9c0cc2bcbec9b7fbd45c4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.9 MB (430873882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4703e7d1b4f1fc5cf047a51e6ab8e41a2834c8ef12407d3c11a13d9ffcb090c`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:57 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 18:59:57 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:57 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 26 Jan 2026 19:18:38 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:18:38 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:18:38 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 26 Jan 2026 19:18:39 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:18:39 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:18:39 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:18:39 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:18:39 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:18:41 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:18:41 GMT
USER gradle
# Mon, 26 Jan 2026 19:18:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:18:42 GMT
USER root
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a07ea5032c792d7ba679b74d72cf278e3e104563477a78ec86bb42a7f99648e`  
		Last Modified: Wed, 21 Jan 2026 19:00:16 GMT  
		Size: 153.4 MB (153367384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e343826650ccbf55f4cca4b45ccc47cefc1cd0bf9110c6bc1ec85ba70c9e2a0`  
		Last Modified: Mon, 26 Jan 2026 19:19:14 GMT  
		Size: 86.0 MB (86040433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ff3fafdf8bbe570677f30c7f8f01997060f5fac9a72c772665e46f243396d1`  
		Last Modified: Mon, 26 Jan 2026 19:19:10 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2dc0394f88403edea681b82c9a9b0e42435ccadc455cb7da351f874b7f5d63`  
		Last Modified: Mon, 26 Jan 2026 19:19:15 GMT  
		Size: 137.4 MB (137388271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b25e1ab6f7791616dfda90b215ead34a8ffd699d7c7b39e32bb4c396370a017`  
		Last Modified: Mon, 26 Jan 2026 19:19:11 GMT  
		Size: 54.9 KB (54909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bb32350505f4246e62c74cfa332b650e7fd54535b345b64b401f55d2c464f521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c57a2fb767c6e215fa877fb844b061479bca5f794def1537b040f43788fe44e`

```dockerfile
```

-	Layers:
	-	`sha256:072c795345280b24224051a8e2ed3c8eda2fd30ff3a8b733ad08c7758c8e2459`  
		Last Modified: Mon, 26 Jan 2026 19:19:11 GMT  
		Size: 11.4 MB (11365982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69609426b40932164298d47e62fad5d619bd21552eb1ce870d83e4e7da4b2b5a`  
		Last Modified: Mon, 26 Jan 2026 19:19:11 GMT  
		Size: 21.5 KB (21523 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:5f5dfb2584b9cb0d1ce2e08bf818000268a4e42159bbf3d90ab13602859ceddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.8 MB (427806415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baaaa8687cd57717fe7d61502c0b056ff48fd113a234c7104c90ebe79972e3be`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:16 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 19:00:16 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:00:16 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 26 Jan 2026 19:19:20 GMT
CMD ["gradle"]
# Mon, 26 Jan 2026 19:19:20 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 26 Jan 2026 19:19:20 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 26 Jan 2026 19:19:20 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 26 Jan 2026 19:19:20 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 26 Jan 2026 19:19:20 GMT
WORKDIR /home/gradle
# Mon, 26 Jan 2026 19:19:20 GMT
ENV GRADLE_VERSION=8.14.4
# Mon, 26 Jan 2026 19:19:20 GMT
ARG GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
# Mon, 26 Jan 2026 19:19:23 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 26 Jan 2026 19:19:23 GMT
USER gradle
# Mon, 26 Jan 2026 19:19:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f1771298a70f6db5a29daf62378c4e18a17fc33c9ba6b14362e0cdf40610380d
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 26 Jan 2026 19:19:24 GMT
USER root
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436dca49d48a119ba29e5c58e3826eb3069953cb00876a3cfc8081de1fdd358b`  
		Last Modified: Wed, 21 Jan 2026 19:00:39 GMT  
		Size: 151.9 MB (151921187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd7406459ea0b9da021a26d5f7b8d1d0134c3021962c9aa87be44c5babadd22`  
		Last Modified: Mon, 26 Jan 2026 19:19:56 GMT  
		Size: 85.5 MB (85521396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea18981ccf804390a6e8d37b40c493963bae5098a94546fb5753d4f3cbef7f8`  
		Last Modified: Mon, 26 Jan 2026 19:19:52 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8ceddf65af10a5032d5d22dc877c6a2b69cc4593004a9c909f82ba82ba83c`  
		Last Modified: Mon, 26 Jan 2026 19:19:58 GMT  
		Size: 137.4 MB (137388270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93bdb6e029fa68a24f03702c2a2052204df6c761c630c1ad4e871345c92b2c0`  
		Last Modified: Mon, 26 Jan 2026 19:19:52 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:2eb8856d507154399872c7f2fc8c8949ca49bd45f7b243e4c2d69b5988086886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11387545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d06a56f22c58a6ac59a9bd1957daea3fa2c67b4517716baabecf8409c110cf`

```dockerfile
```

-	Layers:
	-	`sha256:4d24a389c6341e2fab6a875d895961b78b01db267a9db93051b2011dd44b27a0`  
		Last Modified: Mon, 26 Jan 2026 19:19:53 GMT  
		Size: 11.4 MB (11365825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b09098bee4906221c6a80936e09011fda6e5072026b4d133a434e3477a4e6da`  
		Last Modified: Mon, 26 Jan 2026 19:19:52 GMT  
		Size: 21.7 KB (21720 bytes)  
		MIME: application/vnd.in-toto+json
