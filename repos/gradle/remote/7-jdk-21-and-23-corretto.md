## `gradle:7-jdk-21-and-23-corretto`

```console
$ docker pull gradle@sha256:605ec2ab501cfc9810a9685d80ec5de647cbb52c0052f571cce58686e4f46414
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:7-jdk-21-and-23-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:e60301f5fddcfb80de0cb081754811f12d5e5714de208998c3d03d4802a11fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581286004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db623438a7c7537d88c8e2e7f11d872e7efd1fda7c6cd2810cd0c1231296a36`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 18 Feb 2025 21:10:40 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 18 Feb 2025 21:10:40 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Tue, 18 Feb 2025 21:10:40 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:40 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 18 Feb 2025 21:10:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8588faad644cf783ecb619f9dbb7aa8d78b7fa9c77501b94711a7bba97d2df88`  
		Last Modified: Mon, 10 Feb 2025 20:08:49 GMT  
		Size: 169.8 MB (169753173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c6439b8e1d7fca65c43aee50b5c834503be99970592e1e0c1b403108803ebc`  
		Last Modified: Wed, 19 Feb 2025 21:30:59 GMT  
		Size: 163.5 MB (163481790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ce8b0d8960724495b0b6111bf5d7c8265381a896ac099533eaace3ca21f29f`  
		Last Modified: Wed, 19 Feb 2025 21:30:58 GMT  
		Size: 72.1 MB (72112990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2788aefbf8ea005ac06fe8db0e498c83468bd532893c312262716387ab7fe30`  
		Last Modified: Wed, 19 Feb 2025 21:30:56 GMT  
		Size: 1.8 KB (1756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29547bc06ce14935b4dda9174dea6116886d6608ef1fe9e43ff81647999a91e2`  
		Last Modified: Wed, 19 Feb 2025 21:30:59 GMT  
		Size: 122.8 MB (122785680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-21-and-23-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:94c32d30222ccc73b0c5e3d0639f0239edb9289331b81b8b6f809bffc7eec260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10835697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f629e27c05fc23c52da218646cbe0e17fb817967ef3f3ec8e8d815067b55a1`

```dockerfile
```

-	Layers:
	-	`sha256:ec0c93cb8407ddae01f37dfc96df4326444e930781c6577796fcc6fa8a33d9bf`  
		Last Modified: Wed, 19 Feb 2025 21:30:56 GMT  
		Size: 10.8 MB (10811448 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d3ff03f941ce6c7beb91de47d5b349c8f23e26590f3d7e0bcd3890f5d2bf65b`  
		Last Modified: Wed, 19 Feb 2025 21:30:55 GMT  
		Size: 24.2 KB (24249 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:7-jdk-21-and-23-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:ec8f83af6a53e38c17d7d9556044821ef6566098701545f8c24ebe43fd3a3416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **576.5 MB (576486260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13abbaa699dc76f188e93b808b1a3b721c4b38577ae9a4bd1037dd03bd652a4c`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 18 Feb 2025 21:10:40 GMT
COPY /usr/lib/jvm/java-23-amazon-corretto /usr/lib/jvm/java-23-amazon-corretto # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
ENV JAVA_LTS_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 18 Feb 2025 21:10:40 GMT
ENV JAVA_CURRENT_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Tue, 18 Feb 2025 21:10:40 GMT
CMD ["gradle"]
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && dnf install -y         shadow-utils         unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle         && echo "Ensuring Gradle detects installed JDKs"     && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties     && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Tue, 18 Feb 2025 21:10:40 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 18 Feb 2025 21:10:40 GMT
WORKDIR /home/gradle
# Tue, 18 Feb 2025 21:10:40 GMT
ENV GRADLE_VERSION=7.6.4
# Tue, 18 Feb 2025 21:10:40 GMT
ARG GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
# Tue, 18 Feb 2025 21:10:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=bed1da33cca0f557ab13691c77f38bb67388119e4794d113e051039b80af9bb1
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version # buildkit
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7feeff8a60e4d7d7ae6e10d0a1d0796d8d07a16ed9dad63f734432e89c68d9ce`  
		Last Modified: Mon, 10 Feb 2025 20:27:14 GMT  
		Size: 168.1 MB (168063141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d367addf3b108efd1dbd0a42f73e31043aaa8d79b1616fd19795182c8eed756`  
		Last Modified: Mon, 10 Feb 2025 21:14:52 GMT  
		Size: 161.6 MB (161571516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b631b8437ee3060012575766cd2cb8767e8d7327d8b46eca1a366470319d271f`  
		Last Modified: Mon, 10 Feb 2025 21:14:50 GMT  
		Size: 71.8 MB (71787001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:156c040e28e4916160001448e9681cc300118e0193c59c662b53a4d887084468`  
		Last Modified: Mon, 10 Feb 2025 21:14:48 GMT  
		Size: 1.8 KB (1754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3af33e675583333050bd69e92864e08031c9e3fadbf5ccf95a9a46a1c4848f3`  
		Last Modified: Wed, 19 Feb 2025 22:30:47 GMT  
		Size: 122.8 MB (122791865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:7-jdk-21-and-23-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:4c95e4b618dd138e0b77cd3dd0ded496fca0ecca1428d0cba4f405487d81b099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10833726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369515608930560f911c61cb291b58a1a5f3ed62a4699c8c3a270e15638403c1`

```dockerfile
```

-	Layers:
	-	`sha256:dc23d9e735fba5934f2d5b650a8dd27e1f2cbe14e906f378ff91788adb0d8267`  
		Last Modified: Wed, 19 Feb 2025 22:30:44 GMT  
		Size: 10.8 MB (10809221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80463fc2a423b632a880d6063c26a175e33b710f8cf421fdfbcc04ec20f3176b`  
		Last Modified: Wed, 19 Feb 2025 22:30:43 GMT  
		Size: 24.5 KB (24505 bytes)  
		MIME: application/vnd.in-toto+json
