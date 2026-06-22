## `gradle:9-jdk21-corretto`

```console
$ docker pull gradle@sha256:511fc8b2e6fcf79c52381c9d64ea031e240e389347db876a070d3c7a0f9a696a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk21-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:2d0a4dd1cfad55ceb5b3ffe93e8b5805e41918001efc6e83f7ae238e7624a2ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **452.3 MB (452283959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc226f8b27c2d3183de06b919d96b6bcaa9b7238754f3bb8db673262c05bae5`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:12 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:05:12 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:12 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:12 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 22 Jun 2026 18:15:12 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:15:12 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:15:12 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:15:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:15:12 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:15:12 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:15:12 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:15:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:15:14 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:15:14 GMT
USER gradle
# Mon, 22 Jun 2026 18:15:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:15:15 GMT
USER root
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbda8bbed2402313490b832b371f9a31cefa72cc0c1f79f7de0207d319faaf9`  
		Last Modified: Mon, 22 Jun 2026 18:05:38 GMT  
		Size: 170.4 MB (170446421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23176f41dad1598a774a24bf582bcdcbba97b46edb94dec2e041c304030cd48`  
		Last Modified: Mon, 22 Jun 2026 18:15:42 GMT  
		Size: 86.6 MB (86640954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe41e2449a983c43b536329d194d394b6add30bb4e7ba9e335717a25a7447f54`  
		Last Modified: Mon, 22 Jun 2026 18:15:39 GMT  
		Size: 1.6 KB (1648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e980d587ec2c825a78f7e22dba76900be64e23ca6cd1018808baedb0a09a856`  
		Last Modified: Mon, 22 Jun 2026 18:15:43 GMT  
		Size: 140.6 MB (140595104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2735dde1672b21ece1c7fd985007efa4dfe984b59bdaab1ff6dbeb6285bd7ce6`  
		Last Modified: Mon, 22 Jun 2026 18:15:39 GMT  
		Size: 25.6 KB (25617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:9cb4a5c94111748da5034982a65fa33cc56294ccb1c329d9fd0e44260e88bab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11406710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c87a79496a990e8df0fe48aa125d5dcc0b6f30d7344719b2ceaa836994e5cc`

```dockerfile
```

-	Layers:
	-	`sha256:076c5c98f599e0a83449fab01dfd710fc996557027166f0d4c5e923cd418b393`  
		Last Modified: Mon, 22 Jun 2026 18:15:40 GMT  
		Size: 11.4 MB (11385059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c16da665e10f327ffcfed2dbaf0f927389f0247e2b2fd7562e627c8ade11812`  
		Last Modified: Mon, 22 Jun 2026 18:15:39 GMT  
		Size: 21.7 KB (21651 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk21-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:72fe4bf2d5e65cd03fdd09d0b7e618a2689ef5e9c98bc05f5583d47347f83cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.8 MB (448837536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:313c93d1db25d6361bc3306adf7628d521ea075b1da3861ad46e2c921e25b5dd`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:10 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:15:10 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:10 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:10 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 22 Jun 2026 18:25:47 GMT
CMD ["gradle"]
# Mon, 22 Jun 2026 18:25:47 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 22 Jun 2026 18:25:47 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 22 Jun 2026 18:25:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 22 Jun 2026 18:25:47 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 22 Jun 2026 18:25:47 GMT
WORKDIR /home/gradle
# Mon, 22 Jun 2026 18:25:47 GMT
ENV GRADLE_VERSION=9.6.0
# Mon, 22 Jun 2026 18:25:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
# Mon, 22 Jun 2026 18:25:50 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 22 Jun 2026 18:25:50 GMT
USER gradle
# Mon, 22 Jun 2026 18:25:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bbaeb2fef8710818cf0e261201dab964c572f92b942812df0c3620d62a529a01
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --stacktrace --debug --version # buildkit
# Mon, 22 Jun 2026 18:25:51 GMT
USER root
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10beb5c68f4d3c7d1c45314bbff9c0bb6baf58079563b749b2f64ac9f3c511d3`  
		Last Modified: Mon, 22 Jun 2026 18:15:34 GMT  
		Size: 168.7 MB (168721711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5bd4e55a33f031ed48dfd7ac41723486680fc5d610e558c1558ccac5a58e2b`  
		Last Modified: Mon, 22 Jun 2026 18:26:22 GMT  
		Size: 86.0 MB (86039015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0ccd77005b4fad5d97c286f50c4e759498df577bd5e5714d9e4f67d5e4893c`  
		Last Modified: Mon, 22 Jun 2026 18:26:19 GMT  
		Size: 1.6 KB (1644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2ecb0df8251b5954a578595119f5335c674c4de3ccf78eff77cdd7f2778e6`  
		Last Modified: Mon, 22 Jun 2026 18:26:23 GMT  
		Size: 140.6 MB (140595105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d892128e4a53a85cca1a485d029a89a3ce8eecf686afc7e051c47007aeda5a`  
		Last Modified: Mon, 22 Jun 2026 18:26:19 GMT  
		Size: 29.3 KB (29343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk21-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:b065529646088e5d55f1ffd83d66fe3350bebc53a9831ea2404e261863dadea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11405910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ad918ba271acdf7ee52f1f434ace1a4ad43d569d8c0165e7414bb51caf1c92`

```dockerfile
```

-	Layers:
	-	`sha256:95b4c0f2c75737f1b01db269a2b650f8b16690c2a17b6325ea60c033eecbeaca`  
		Last Modified: Mon, 22 Jun 2026 18:26:19 GMT  
		Size: 11.4 MB (11384062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2700de21be5980fc75063bf6cb604e1e12059cb609b3ad688309682c2b1aa108`  
		Last Modified: Mon, 22 Jun 2026 18:26:18 GMT  
		Size: 21.8 KB (21848 bytes)  
		MIME: application/vnd.in-toto+json
