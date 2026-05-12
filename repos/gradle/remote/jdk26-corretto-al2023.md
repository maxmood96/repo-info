## `gradle:jdk26-corretto-al2023`

```console
$ docker pull gradle@sha256:8fb3323cec7fddc5507c3cb2ee372b0f27b59a982913ad65f7ec5f92dd29c021
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk26-corretto-al2023` - linux; amd64

```console
$ docker pull gradle@sha256:0ed5233c986888ff96a682062b000f21fa52fdcaf603f06e2860d63ea2d1db8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **474.5 MB (474456304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995c81ddc6bdb019a96f3921fdb8723b79af13274ac6ffed00b0f0fa7dc91223`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:19:34 GMT
ARG version=26.0.1.8-1
# Sat, 09 May 2026 00:19:34 GMT
ARG package_version=1
# Sat, 09 May 2026 00:19:34 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:19:34 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:19:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Tue, 12 May 2026 20:49:53 GMT
CMD ["gradle"]
# Tue, 12 May 2026 20:49:53 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 20:49:53 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 12 May 2026 20:49:53 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 20:49:53 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 20:49:53 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 20:49:53 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 20:49:53 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:49:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:49:56 GMT
USER gradle
# Tue, 12 May 2026 20:49:56 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:49:56 GMT
USER root
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b7a72c98e682d1076395e72f4c530a217dc9630b3d728f95711cc26484bec0`  
		Last Modified: Sat, 09 May 2026 00:19:59 GMT  
		Size: 193.4 MB (193449243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b7fa797976b65c8084689f93374e2a9877414960b0f5f3eda4ce7fd9b6f99c`  
		Last Modified: Tue, 12 May 2026 20:50:29 GMT  
		Size: 86.2 MB (86165980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07433a98b7f0c239bf9995e2b97cc7aa5ca4f30f41b9a4e900e899a8d659d6a`  
		Last Modified: Tue, 12 May 2026 20:50:25 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78679812369d2414f635a1afa56710185adc68be7ecbda2f0dd1b61be4b5d2a6`  
		Last Modified: Tue, 12 May 2026 20:50:32 GMT  
		Size: 140.2 MB (140236985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73c339643d0d544c8add803c253d88ff053a15df1becb62ead957a482190acc`  
		Last Modified: Tue, 12 May 2026 20:50:25 GMT  
		Size: 25.6 KB (25612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:606b548d043e48a30f29ec575f06ebaf635b8e2bd33093a7a8180e277a46cede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11397197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4258efc12fc9ab9d33587a6f290dbbbd3be832e2b7e2b6386e8ab8a7a1c891a1`

```dockerfile
```

-	Layers:
	-	`sha256:f088f0dee7c03da1dffccbc0372c7e410284753279d28a33ab19d4472b827d49`  
		Last Modified: Tue, 12 May 2026 20:50:26 GMT  
		Size: 11.4 MB (11375546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ddb3af059a8b0551365d637e56572123db9d385c5d54d97ba8faf55937dec2e`  
		Last Modified: Tue, 12 May 2026 20:50:25 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk26-corretto-al2023` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:90fd5e2721348a7e2298e462b5a74a2335decb285b36633801607d4b5f11633c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.7 MB (470660256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837da01adf3e22fd0790bb339e22862bfb30bb5f53449a7b054e3d1af08fda17`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:53 GMT
ARG version=26.0.1.8-1
# Sat, 09 May 2026 00:16:53 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:53 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:53 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
# Tue, 12 May 2026 20:48:13 GMT
CMD ["gradle"]
# Tue, 12 May 2026 20:48:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 12 May 2026 20:48:13 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 12 May 2026 20:48:13 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Tue, 12 May 2026 20:48:13 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 12 May 2026 20:48:13 GMT
WORKDIR /home/gradle
# Tue, 12 May 2026 20:48:13 GMT
ENV GRADLE_VERSION=9.5.1
# Tue, 12 May 2026 20:48:13 GMT
ARG GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
# Tue, 12 May 2026 20:48:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Tue, 12 May 2026 20:48:16 GMT
USER gradle
# Tue, 12 May 2026 20:48:16 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bafc141b619ad6350fd975fc903156dd5c151998cc8b058e8c1044ab5f7b031f
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Tue, 12 May 2026 20:48:16 GMT
USER root
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb374f78b6fea07d5aa41abdb8393d250b82aa0fe84ab4cbca9d0fa9c26c6c6`  
		Last Modified: Sat, 09 May 2026 00:17:20 GMT  
		Size: 191.3 MB (191273814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a37ce4cac4ef119faeb851de942b495f5ac9fa518772857a83e28b07c42210`  
		Last Modified: Tue, 12 May 2026 20:48:48 GMT  
		Size: 85.7 MB (85661468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8609394dc28f69025f157c4c3fb8c6101c38bf3d2d10bb4b09b291dae971827`  
		Last Modified: Tue, 12 May 2026 20:48:45 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68aac54a8c7b4bbed181a05a03210b1d475c411eebebdc0e64b0f14afbe4916`  
		Last Modified: Tue, 12 May 2026 20:48:50 GMT  
		Size: 140.2 MB (140236984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e377eb82078bf981680a797b1f73f4e182cec9d8ed131e2b790830b4b1313f`  
		Last Modified: Tue, 12 May 2026 20:48:45 GMT  
		Size: 29.3 KB (29335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk26-corretto-al2023` - unknown; unknown

```console
$ docker pull gradle@sha256:92c04ca9c86fff3fab6c2b8f8142e4ec3b5ef9fcae242b764a813211cf0ba5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11396403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0969a29b4ed635d9ef27d6526773acb7aaa67f361887d0226160929e140dbfa`

```dockerfile
```

-	Layers:
	-	`sha256:7f0f68131ea2815989586ffecf2f2ae520f9021cfde2647762be8e4902e9e87c`  
		Last Modified: Tue, 12 May 2026 20:48:46 GMT  
		Size: 11.4 MB (11374555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d803bcb153f0b1adbebd60b3063218722c9e987afa79f308cd56d54996e075`  
		Last Modified: Tue, 12 May 2026 20:48:45 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
