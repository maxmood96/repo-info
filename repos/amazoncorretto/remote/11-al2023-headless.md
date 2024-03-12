## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:a5a749669b4d20e00bf34ed20aeec62cb24e53d6c7941f766e307176ef62ace2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:074c0003d62bc23e5bb7f4015f349bf3a6dddc7b6eeae2f3840e39270620e272
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128265257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4f2e42b02d0301b82a46bf20a49b3b8908945ae696319a4210e7345570815e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 22:51:53 GMT
COPY dir:fa03cac066e59421bfc5bec4359b41f98285f388dfc0f4cb40cc2ee361147dfd in / 
# Mon, 26 Feb 2024 22:51:53 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:11:59 GMT
ARG version=11.0.22.7-1
# Mon, 26 Feb 2024 23:12:44 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 26 Feb 2024 23:12:44 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:12:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8784573bb84d178812057375084b2df4e8a0ffb22734f522709063f9581c296f`  
		Last Modified: Tue, 20 Feb 2024 01:09:31 GMT  
		Size: 52.2 MB (52210179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511d2abb3dd937fb95ebcd6bec2a2815cc0be3c96a0b42075c86e63ecc562322`  
		Last Modified: Mon, 26 Feb 2024 23:25:50 GMT  
		Size: 76.1 MB (76055078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:555411e10cb2db6ba02f8ef1a66c6a4433622e30ec6572e58e1adbc0176e4974
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126640440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd817932c0ab58269308b85deace41b81a6ebecb95d7f9672ee3b41b11740cf1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 Mar 2024 22:39:43 GMT
COPY dir:2bac3e0f2f9808be2259a0eea507562cc31d6f7cf5f26809139e8bb63fb6b535 in / 
# Mon, 11 Mar 2024 22:39:44 GMT
CMD ["/bin/bash"]
# Mon, 11 Mar 2024 23:12:13 GMT
ARG version=11.0.22.7-1
# Mon, 11 Mar 2024 23:12:50 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 11 Mar 2024 23:12:51 GMT
ENV LANG=C.UTF-8
# Mon, 11 Mar 2024 23:12:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:89bff426afee4c835c6855932ea2864aef333271964dcfe8c4e0cd4be90649f8`  
		Last Modified: Wed, 06 Mar 2024 01:18:22 GMT  
		Size: 51.4 MB (51406909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3077071ea05288d03a84ffb8d5693631a60c7ffecd3f24be44f0e87fda7c06b7`  
		Last Modified: Mon, 11 Mar 2024 23:22:39 GMT  
		Size: 75.2 MB (75233531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
