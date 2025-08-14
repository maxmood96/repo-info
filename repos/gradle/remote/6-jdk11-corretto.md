## `gradle:6-jdk11-corretto`

```console
$ docker pull gradle@sha256:7efdc3abdcf4566257bfa8b1c6b32abf03e924c59c0754621cf31696a4c5a249
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:6-jdk11-corretto` - linux; amd64

```console
$ docker pull gradle@sha256:767edbab97c351c6057986adf6e91f2b087f548d5dfaac5e9ffc3e0c659ad147
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 MB (401587566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6510d99387aa222c8f0959e69a35f91c2be6139237788d91315e0b9e729bc631`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Jun 2025 18:02:05 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["/bin/bash"]
# Mon, 02 Jun 2025 18:02:05 GMT
ARG version=11.0.28.6-1
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV LANG=C.UTF-8
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:b9bd06b1e98f2884554d02055b944634294fa4d6f341ec4d0d7349c492676b31`  
		Last Modified: Sat, 09 Aug 2025 04:12:21 GMT  
		Size: 53.8 MB (53837959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec828ce5d2d44eda954aac728695e0e891c8a7cd07cc61c3e2be05880101eaf`  
		Last Modified: Wed, 13 Aug 2025 23:11:17 GMT  
		Size: 154.1 MB (154063982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef12d664948a8282df745a1f931cecdf5ec5f351c60e63431227c17c52b6ba27`  
		Last Modified: Wed, 13 Aug 2025 23:12:52 GMT  
		Size: 85.6 MB (85556014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b023e00026d9605bda7a95f22728939583a36f6ecc101de981ca21a322f487`  
		Last Modified: Wed, 13 Aug 2025 23:12:48 GMT  
		Size: 1.6 KB (1643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb32155054059dd67b6a8c745e18a045e668a72805c07ad595c752fe398c1fb7`  
		Last Modified: Thu, 14 Aug 2025 02:17:41 GMT  
		Size: 107.7 MB (107696662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec4ce77d2cf81219cb454e6701fa5317d4a399c7a4ad2f0c5d5b0619218a4ac`  
		Last Modified: Thu, 14 Aug 2025 02:09:53 GMT  
		Size: 431.3 KB (431274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:1f924960acb34fc4a1540a97ecbef4b057ebf016714baa266045cd83bb5364bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11250659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588e8ad228f8e53ca789a676d49d6adc7fc4f60872547952182bffb4c0096c8e`

```dockerfile
```

-	Layers:
	-	`sha256:56934b3017dc1fc1d9eced3949cbf77cc52552ad1f593a3ffdb3bbd1af1bcfd1`  
		Last Modified: Thu, 14 Aug 2025 02:17:23 GMT  
		Size: 11.2 MB (11229728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7b274b724ea2c0ae7da228cf5390a6ae20b82cb007b9027e6e166955ae20154`  
		Last Modified: Thu, 14 Aug 2025 02:17:24 GMT  
		Size: 20.9 KB (20931 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:6-jdk11-corretto` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:420e3d27587d7d475a34ce9f66452791f1da827e94973617bf21de0c6168b337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.5 MB (398496251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0434c7e9602860148488e9e45f4bb5c59d23658ed3170be623f28611f44fdb7b`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 02 Jun 2025 18:02:05 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["/bin/bash"]
# Mon, 02 Jun 2025 18:02:05 GMT
ARG version=11.0.28.6-1
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
ENV LANG=C.UTF-8
# Mon, 02 Jun 2025 18:02:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 02 Jun 2025 18:02:05 GMT
CMD ["gradle"]
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && dnf install -y         make         tar                 unzip         wget         which                 findutils                 git         git-lfs         mercurial         subversion     && dnf clean all     && rm -rf /var/cache/yum         && echo "Testing common utilities"     && which awk     && which curl     && which cut     && which grep     && which gunzip     && which sha256sum     && which sed     && which tar     && which tr     && which unzip     && which wget         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle     && chmod --recursive o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 02 Jun 2025 18:02:05 GMT
WORKDIR /home/gradle
# Mon, 02 Jun 2025 18:02:05 GMT
ENV GRADLE_VERSION=6.9.4
# Mon, 02 Jun 2025 18:02:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER gradle
# Mon, 02 Jun 2025 18:02:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=3e240228538de9f18772a574e99a0ba959e83d6ef351014381acd9631781389a
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Mon, 02 Jun 2025 18:02:05 GMT
USER root
```

-	Layers:
	-	`sha256:93b5cbbc86ee614f8432762e1f7f34b6cc9d6d4b95867cf25bca6ae179f49439`  
		Last Modified: Sat, 09 Aug 2025 04:12:37 GMT  
		Size: 52.7 MB (52726394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20183faf628bb3bf8416e2bff502cb48f4f73fb58cc8166653501de1e32f063`  
		Last Modified: Thu, 14 Aug 2025 11:54:11 GMT  
		Size: 152.6 MB (152569365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57671592cd1d35145352056ee73db79d1fd820835ecc98e125d65093ad571e81`  
		Last Modified: Thu, 14 Aug 2025 20:08:37 GMT  
		Size: 85.1 MB (85077119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82abd31a8d1a670a031036de770e9e28db849b00b53cead4439d2ac663269c51`  
		Last Modified: Thu, 14 Aug 2025 17:26:34 GMT  
		Size: 1.6 KB (1649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c3cbe0e770c0ad91a6f3e518b97b66478bc5af7588b89ca8329e90bfab8a75`  
		Last Modified: Thu, 14 Aug 2025 17:25:43 GMT  
		Size: 107.7 MB (107696664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2accf2b4ddd1298c941717d811b7b3b3fe6853296fa0313c7afefe9a8e602bb4`  
		Last Modified: Thu, 14 Aug 2025 17:26:34 GMT  
		Size: 425.0 KB (425028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:6-jdk11-corretto` - unknown; unknown

```console
$ docker pull gradle@sha256:4f220e0491eaf6acd2ca8688a317c5fe643dcc1f807f5e183db577c8bbdf79e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11250635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5f29c88bd8746a9b299dd40ac8b5127efd345f3e567b04540cb3c085758f044`

```dockerfile
```

-	Layers:
	-	`sha256:c98be123e5cdccfab5fe0fe9343e4e94c6b8651a8829e48928bb5843de389bd7`  
		Last Modified: Thu, 14 Aug 2025 20:17:33 GMT  
		Size: 11.2 MB (11229547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e9e9c9614598d512be2b209afc8e62af6f035407eeeb924ea1857d1a9818ba4`  
		Last Modified: Thu, 14 Aug 2025 20:17:34 GMT  
		Size: 21.1 KB (21088 bytes)  
		MIME: application/vnd.in-toto+json
