## `gradle:9-jdk-25-and-25-corretto`

```console
$ docker pull gradle@sha256:33d48bf263f9922d99992caa2449c6591e650476aaa7525a93577f5635e8b057
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:9-jdk-25-and-25-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:b1011e90b5e5b2fb3bf445e8a5fac639ae1781b118046a554052977a513c3d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **464.4 MB (464356184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a38e8a0aa490f6cafde7599d9e4c6ef5b04bb2f1a3a5675f7ce23280a408c22`
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
# Fri, 31 Oct 2025 01:11:30 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:11:30 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:11:30 GMT
CMD ["gradle"]
# Fri, 31 Oct 2025 01:11:30 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 31 Oct 2025 01:11:30 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Fri, 31 Oct 2025 01:11:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Fri, 31 Oct 2025 01:11:30 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 31 Oct 2025 01:11:30 GMT
WORKDIR /home/gradle
# Fri, 31 Oct 2025 01:11:30 GMT
ENV GRADLE_VERSION=9.2.0
# Fri, 31 Oct 2025 01:11:30 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Fri, 31 Oct 2025 01:11:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
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
	-	`sha256:230e862c5281f22f664b7a1113d0b517bf4bb3fdc55d83e76bcc7b13158ee2ea`  
		Last Modified: Fri, 31 Oct 2025 01:12:17 GMT  
		Size: 85.6 MB (85613005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb20f863c5e3f2fb3104e62374fdc0f66fcc25cb5f07fc2cf0aaa57d904bbb8`  
		Last Modified: Fri, 31 Oct 2025 01:12:09 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166abdb79215b3e5a62b645dd0bb31fca7340ee7a3f4011de09893b4c9ef384e`  
		Last Modified: Fri, 31 Oct 2025 04:46:44 GMT  
		Size: 135.6 MB (135574554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:03d78c1cce22888c4b3897c8cd5591712dd894d5d5919ee6c0ad92056316521c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11354742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee494611d063f3fee4747a083e003a3f83317aabae3e7250edcc005aa139dcea`

```dockerfile
```

-	Layers:
	-	`sha256:b2e81b259e9f80c9727b2c65789a26845bd112c1b3aa5fe5031022281d711b4e`  
		Last Modified: Fri, 31 Oct 2025 02:22:53 GMT  
		Size: 11.3 MB (11330303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:302c4e2cb57f1b61ddcde3186f45512dd91c84434a3c6cccdea3bd6c3c19f89a`  
		Last Modified: Fri, 31 Oct 2025 02:22:54 GMT  
		Size: 24.4 KB (24439 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:9-jdk-25-and-25-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:84e2bbc9216f905b6d727546e3077069bb8ea6a689a860575ac24453dbba40fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **460.7 MB (460743903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9789b52d8240da8289781f0626f7f4ccaf76c0454b4561c2560fdd5a896ecb`
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
# Tue, 04 Nov 2025 23:26:00 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 04 Nov 2025 23:26:00 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 04 Nov 2025 23:26:00 GMT
CMD ["gradle"]
# Tue, 04 Nov 2025 23:26:00 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 04 Nov 2025 23:26:00 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         curl-minimal         wget         tar                 unzip         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 04 Nov 2025 23:26:01 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 04 Nov 2025 23:26:01 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 04 Nov 2025 23:26:01 GMT
WORKDIR /home/gradle
# Tue, 04 Nov 2025 23:26:01 GMT
ENV GRADLE_VERSION=9.2.0
# Tue, 04 Nov 2025 23:26:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
# Tue, 04 Nov 2025 23:26:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=df67a32e86e3276d011735facb1535f64d0d88df84fa87521e90becc2d735444
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
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
	-	`sha256:4c42ef8cf0c1d733d48238d1eb1748e2afc05256ac1ad1d4e503f235a9dee576`  
		Last Modified: Tue, 04 Nov 2025 23:26:53 GMT  
		Size: 85.2 MB (85166189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a45f25c1fd21bbfbf0fe4c33b178dd1e96e641b853352eddbaed9df47cb7f2`  
		Last Modified: Tue, 04 Nov 2025 23:26:44 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c5429777773f5612c545fec3e2e524a60257983f88b5d493f3d4bdccd69292`  
		Last Modified: Tue, 04 Nov 2025 23:26:37 GMT  
		Size: 135.6 MB (135581822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:9-jdk-25-and-25-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:bf04e5506cc9fd8967afa55aaec67eb0999f4158ba2dc8c5b0a6a48dec3b4acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11354128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1ca398f605bccc501cd3f0e698c7f14795b5fa2db284cefc79c65c6e90d271`

```dockerfile
```

-	Layers:
	-	`sha256:7d76873507dee5b6495cc068e5dd61df42b3b71e4743f12985196425eb393822`  
		Last Modified: Wed, 05 Nov 2025 00:21:00 GMT  
		Size: 11.3 MB (11329412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:795ff4dde9f13609897503bada93cb2d23868a736952dd72a54c88b3689d56cb`  
		Last Modified: Wed, 05 Nov 2025 00:21:01 GMT  
		Size: 24.7 KB (24716 bytes)  
		MIME: application/vnd.in-toto+json
