## `gradle:jdk-21-and-24-corretto`

```console
$ docker pull gradle@sha256:aa2c3f71ed26daf7f5c087e07d07263968de3ec50a05e8634ed4d7f2a79c3048
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:jdk-21-and-24-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:eaef0ee4bfe072fc4dc12f501190b33802c89d1420d3ef8db5cc90ab2636bba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **617.2 MB (617181927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b055381009ae80ee9e44b3cd94e0a417dccb3b9f54337b4b80db8869d12da46`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:b9bd06b1e98f2884554d02055b944634294fa4d6f341ec4d0d7349c492676b31`  
		Last Modified: Sat, 09 Aug 2025 04:12:21 GMT  
		Size: 53.8 MB (53837959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6060431010add9e3f62b68ab8eeaa3923d86c2e7bc50971d98551fd060b8fb5c`  
		Last Modified: Wed, 13 Aug 2025 23:11:02 GMT  
		Size: 170.1 MB (170103636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d3dcf81e2f81f9d67fdd47c226471764735337ab041e51864787b05187897`  
		Last Modified: Thu, 14 Aug 2025 00:14:25 GMT  
		Size: 173.1 MB (173149204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc37778505257948182d47c0b5ed9ca7a048c309f3db5cfb9f1366d81f756e`  
		Last Modified: Thu, 14 Aug 2025 00:14:32 GMT  
		Size: 85.6 MB (85553292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f183f02158cff9c24990cb4125ae47f198c296246c1e3ad7760b3bdbe48a39e5`  
		Last Modified: Wed, 13 Aug 2025 23:37:30 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b68d87e427fb8d26774075ffd020cebe76b9c32ce4e965e5f87290681e4416`  
		Last Modified: Thu, 14 Aug 2025 00:14:41 GMT  
		Size: 134.5 MB (134536049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:555f20f2e679a84d5020e65b8c9b2d2016ff02b5a32d060db6e9601bf9a671c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11495584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da5221276df036c09505e011487cde15220dd08ebb9a87970284d2e7aa4419f4`

```dockerfile
```

-	Layers:
	-	`sha256:89245d3e3ba0cb5f8c2a8ce99c021f1a799a76a1e0a04f4b3bb25273186c45a4`  
		Last Modified: Thu, 14 Aug 2025 02:24:33 GMT  
		Size: 11.5 MB (11468302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d237a6baf05ace6e2da590b6b5b808a29ac374195b6d99568e246b6425c3815`  
		Last Modified: Thu, 14 Aug 2025 02:24:34 GMT  
		Size: 27.3 KB (27282 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:jdk-21-and-24-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:f1990dbaf1597fe73ba8847d6fc38e23eb52404bb6b32cd9ed8b7d141e3e3089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.0 MB (611970960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0349ec0ae0e06bb64e78109aab86481309a7d5c594f86a988a38a1f0228e6c32`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
COPY /usr/lib/jvm/java-24-amazon-corretto /usr/lib/jvm/java-24-amazon-corretto # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 31 Jul 2025 17:27:11 GMT
CMD ["gradle"]
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Thu, 31 Jul 2025 17:27:11 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 31 Jul 2025 17:27:11 GMT
WORKDIR /home/gradle
# Thu, 31 Jul 2025 17:27:11 GMT
ENV GRADLE_VERSION=9.0.0
# Thu, 31 Jul 2025 17:27:11 GMT
ARG GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
# Thu, 31 Jul 2025 17:27:11 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8fad3d78296ca518113f3d29016617c7f9367dc005f932bd9d93bf45ba46072b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4791018861dbdd39eab0020dc251b37b20560bdc5da4d02a1f1dcf5b81c6fb8`  
		Last Modified: Thu, 14 Aug 2025 09:58:31 GMT  
		Size: 168.4 MB (168390174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b62f5629af630ff4758cdeadf1dde5c2d67235f07e6ec817546bb9a4c8641`  
		Last Modified: Thu, 14 Aug 2025 11:22:09 GMT  
		Size: 171.2 MB (171230926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efac254095b93ec29560007d9c157028ee4614386e4ecc4d67162afe50ad052d`  
		Last Modified: Thu, 14 Aug 2025 11:23:22 GMT  
		Size: 85.1 MB (85079682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c0e298d6bf57537fbc3866e376aa477daf28c9452e1bceea0312922fa51f9b`  
		Last Modified: Thu, 14 Aug 2025 11:23:03 GMT  
		Size: 1.8 KB (1755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ea2d895880e99fb51565e030fb0671b0a3bc58b180bc6fac6c8488de28f7f1`  
		Last Modified: Thu, 14 Aug 2025 11:22:09 GMT  
		Size: 134.5 MB (134541997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:jdk-21-and-24-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:59de4c6b20ce29d2f00ff5495863c098979f42d9c4629847bd5f3646237e212c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11494346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033212ebd7ab8c1eca53a7158b3dcc72f2185969c58465f7e573067c0e3a22d1`

```dockerfile
```

-	Layers:
	-	`sha256:b37751949c31982d18132672bb749b00b6e8893520ca45e2acb298ad05e11f53`  
		Last Modified: Thu, 14 Aug 2025 14:24:35 GMT  
		Size: 11.5 MB (11466760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e823b5ffa42cdadc4c7772dc846c58b25f4673b1bed65e4cf58c9ce9b112800d`  
		Last Modified: Thu, 14 Aug 2025 14:24:36 GMT  
		Size: 27.6 KB (27586 bytes)  
		MIME: application/vnd.in-toto+json
