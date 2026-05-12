## `gradle:9-jdk25-corretto`

```console
$ docker pull gradle@sha256:ce97b7b1e3e51c0bfb0c9b4e88216f588b072cb01afd04a1c431f0bc0ad5691f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:f0091634678f73520e731359337f420b5f17d3d2f4d44b21b7f882997e0302f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.4 MB (470422215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9852f1b3aeed5ad32612e4e3794ee874f950e7360b8941963e3f3db16771dc`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:19:00 GMT
ARG version=25.0.3.9-1
# Sat, 09 May 2026 00:19:00 GMT
ARG package_version=1
# Sat, 09 May 2026 00:19:00 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:19:00 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:19:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 12 May 2026 20:47:46 GMT
CMD ["gradle"]
# Tue, 12 May 2026 20:47:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 20:47:46 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 12 May 2026 20:47:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 20:47:47 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 20:47:47 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 20:47:47 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 20:47:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:47:49 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:47:49 GMT
USER gradle
# Tue, 12 May 2026 20:47:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:47:50 GMT
USER root
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0250ec3d728132a010a8ee425e754a8d5a13a96838c49f810421351398ab603e`  
		Last Modified: Sat, 09 May 2026 00:19:24 GMT  
		Size: 189.4 MB (189411044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72caffa232016110a416f8b48fa30686dde306a6f462ef6f698e3307cfbb9db0`  
		Last Modified: Tue, 12 May 2026 20:48:21 GMT  
		Size: 86.2 MB (86170090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8911466e05b61627d365ea633bee3d01b61f18c2033c6c15a5bcbd2d1f4009a3`  
		Last Modified: Tue, 12 May 2026 20:48:17 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c0725e6a55f05d06c47550780ced4336676a7e584f842ae589c0d85ef30369`  
		Last Modified: Tue, 12 May 2026 20:48:22 GMT  
		Size: 140.2 MB (140236986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d763bbf173a4ed98d51712bc2682abed4ae7669938310365b99a553223188f75`  
		Last Modified: Tue, 12 May 2026 20:48:17 GMT  
		Size: 25.6 KB (25612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:5a178eb699c2a114a3066bc2bdd3debaeaa06776d52f18995ae6a4a9a42197cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11402524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2e5818436549bbea9ea11489c836e9fa60d3c72de805eb07d21f39a4a30afd`

```dockerfile
```

-	Layers:
	-	`sha256:11464d71b27882a2783841dfcc150f2b9c5a3882967fffd8a19df5dca27051aa`  
		Last Modified: Tue, 12 May 2026 20:48:18 GMT  
		Size: 11.4 MB (11380255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b4ab84e734ac7bd9dabd19ac12fe7423068e03cb7beec39d38e27dcca066ed`  
		Last Modified: Tue, 12 May 2026 20:48:17 GMT  
		Size: 22.3 KB (22269 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:75a321f169714156e5000afd437f42d9cee91c1abd4145603f6cb05235d34139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **466.7 MB (466719115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271d797b146ef800e7b2527bf1ece65d0e62085ee848ca0477f1b04030cb0860`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:48 GMT
ARG version=25.0.3.9-1
# Sat, 09 May 2026 00:16:48 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:48 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:48 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 12 May 2026 20:47:44 GMT
CMD ["gradle"]
# Tue, 12 May 2026 20:47:44 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 20:47:44 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 12 May 2026 20:47:44 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 20:47:44 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 20:47:44 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 20:47:44 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 20:47:44 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:47:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:47:47 GMT
USER gradle
# Tue, 12 May 2026 20:47:48 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:47:48 GMT
USER root
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650af40d683d967f6be2238c5da49e6232e999e2dbcf6f6803931dde1fea81a8`  
		Last Modified: Sat, 09 May 2026 00:17:16 GMT  
		Size: 187.3 MB (187330634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c54d42a064edacce64681c60482d69b52b21b1a1777cd3f9ec88c77f69a6e8`  
		Last Modified: Tue, 12 May 2026 20:48:19 GMT  
		Size: 85.7 MB (85663506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c698acc5d12be42ba5c471d066d8e4686fe09183b6436d5ee4a6d1a68e35ad6`  
		Last Modified: Tue, 12 May 2026 20:48:16 GMT  
		Size: 1.6 KB (1645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78cc082c887e10c08e133e4e38c8237885c69d590c5e3b888813067fe0a5dfdc`  
		Last Modified: Tue, 12 May 2026 20:48:21 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b38760cd70337d9cf687020be08442742d9bb8920a1460548c23789ffceb30`  
		Last Modified: Tue, 12 May 2026 20:48:16 GMT  
		Size: 29.3 KB (29338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:8df253e3a93b9b1f8ba75a8e23a36255dd9bda2daca2bcecd9575ea30e9af7bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11401783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0467280fa02859109eff3e4712cb719c9762e788ed40fa3db6b1c42dedf1803`

```dockerfile
```

-	Layers:
	-	`sha256:ffa2d8331ab84cf6c707ffae3e33a8be600edd46f4b9dec6311ccb8a39c226b9`  
		Last Modified: Tue, 12 May 2026 20:48:17 GMT  
		Size: 11.4 MB (11379293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a70d052e8899c85150f7f52f7819fa1aad2581ba1a79dc57249dd5e75ee44d8`  
		Last Modified: Tue, 12 May 2026 20:48:16 GMT  
		Size: 22.5 KB (22490 bytes)  
		MIME: application/vnd.in-toto+json
