## `gradle:8-jdk23-corretto`

```console
$ docker pull gradle@sha256:b3f003618b10a62fd1aacf00d81e8ea96205330c9c8a557192a5e0340819543a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk23-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:3cebea5b476b70a0a815950a46889514ae753c3c43360fb4930e8aab69928f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.3 MB (437282520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d220519f39cd48b2d483eb65147707cdfc302c56aa2315bdf0cb553f723ec85`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Wed, 06 Nov 2024 04:13:47 GMT
CMD ["gradle"]
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Nov 2024 04:13:47 GMT
WORKDIR /home/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 06 Nov 2024 04:13:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER gradle
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER root
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63432d46f0bf9dcc129c24c901e228dcb4238fd6c3d3049c5cdb5418c717d991`  
		Last Modified: Mon, 21 Oct 2024 18:57:31 GMT  
		Size: 177.5 MB (177514361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c74a660ae3f966e63199320e639a59b5611892baa51542954caedb59583685a`  
		Last Modified: Wed, 06 Nov 2024 20:17:45 GMT  
		Size: 70.6 MB (70638006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a1a2e63f29189ac407a4aa14e5e1dab4a864463142b082dee3c3da3c3cbd49`  
		Last Modified: Wed, 06 Nov 2024 20:17:44 GMT  
		Size: 1.6 KB (1646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4c39d808c8fdea5e7f3d7c3f8e82c1edb77bbaaec6d41c1a9ef63165dbe080`  
		Last Modified: Wed, 06 Nov 2024 20:17:46 GMT  
		Size: 136.7 MB (136729733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8c0ae74bf6b924313ece795ea71fe1e72f92351ecf998c0675cb01d1aa2658`  
		Last Modified: Wed, 06 Nov 2024 20:17:44 GMT  
		Size: 54.9 KB (54910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:52a7c95e19e1e7a4c2cf05edf12dc28953ea95949d9550e4f5398d2a3d1208c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10752855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b88f658de3a3796d35a26cc9106e2af240f6260f0f7a67269808574ef524d72`

```dockerfile
```

-	Layers:
	-	`sha256:363cbb833bcfd4bdb782a7444cc764a0619e7adf624578b09a83b38551cc2e60`  
		Last Modified: Wed, 06 Nov 2024 20:17:44 GMT  
		Size: 10.7 MB (10734287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939b0a540f54cd6616da8d8c85da6cf7ee38746ba491aab1e98ef2f75abee998`  
		Last Modified: Wed, 06 Nov 2024 20:17:44 GMT  
		Size: 18.6 KB (18568 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk23-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:9ea5a0df7d8dc933b118aec728d2c5cb39db15bb59891d3c5efb9b60fb60bd54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.0 MB (434042043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c66d7f62493f362c9340f004611e3cfba5e4b2600efd3aba7840be44ddb398`
-	Default Command: `["gradle"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Wed, 06 Nov 2024 04:13:47 GMT
CMD ["gradle"]
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 06 Nov 2024 04:13:47 GMT
WORKDIR /home/gradle
# Wed, 06 Nov 2024 04:13:47 GMT
ENV GRADLE_VERSION=8.10.2
# Wed, 06 Nov 2024 04:13:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER gradle
# Wed, 06 Nov 2024 04:13:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Wed, 06 Nov 2024 04:13:47 GMT
USER root
```

-	Layers:
	-	`sha256:923a2071aa1c62af0f57aa46e86e64587ba93da0a38eaf52d228227154730e17`  
		Last Modified: Tue, 15 Oct 2024 02:53:59 GMT  
		Size: 51.4 MB (51424527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e0117da74cb7cbe9ad9f0360b21d6925117299fd6467e13ea320d225cf2708`  
		Last Modified: Mon, 21 Oct 2024 21:06:48 GMT  
		Size: 175.5 MB (175489634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14ded5a8f0b6ce91d03c20c9c2c319b05640183cf12cb86792b7d48efadc452`  
		Last Modified: Wed, 06 Nov 2024 20:14:27 GMT  
		Size: 70.3 MB (70336939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f215cfdb10d3b45dae50cee3b37c0e592b275df239afcbe74125c582a86c9b`  
		Last Modified: Wed, 06 Nov 2024 20:14:24 GMT  
		Size: 1.6 KB (1647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7140c33cbd89a6a6f0098142e582ff6e42a3386d196f6de7841a09481da8fe7e`  
		Last Modified: Wed, 06 Nov 2024 20:14:28 GMT  
		Size: 136.7 MB (136729736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d624c47fed791b067e2bc67d0249303e5331731d52aeca71af4c8865f020cd0`  
		Last Modified: Wed, 06 Nov 2024 20:14:24 GMT  
		Size: 59.5 KB (59528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk23-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:3d5acceef79357d0529d233e133a3e6c1b2439d15c03e9fec5789db0653425f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10751142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402721eca8e66f9e04eb99041e7a2e776137a39434330e8fc12e90f82f5e4d8b`

```dockerfile
```

-	Layers:
	-	`sha256:2844d0c2ce68010876da93808cc9a25902d095134146fb94e22713e2d589b8ff`  
		Last Modified: Wed, 06 Nov 2024 20:14:25 GMT  
		Size: 10.7 MB (10732425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf6d72f93cc82fdd7403315337869378960cc2030ad287190ff8935844e6b7d`  
		Last Modified: Wed, 06 Nov 2024 20:14:24 GMT  
		Size: 18.7 KB (18717 bytes)  
		MIME: application/vnd.in-toto+json
