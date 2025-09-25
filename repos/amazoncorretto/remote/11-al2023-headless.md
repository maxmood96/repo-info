## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4e31c3fc41329fbaebf7826d59c19ddc4d3d21c77ea14cb1143ac3bdca802b57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6d6411773548077f1e89789d2a1c3a6478d875b8846ec587bc5d3cd4164402ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130389276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b91f06444280356b63ee8d052fddba639c071efb7988a791983c87f0d6cc03a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5f2889525a5b46c999ff4ccb86ab3c3d7271ebf69dbdbf70b03c6ed67bb865`  
		Last Modified: Thu, 25 Sep 2025 02:15:26 GMT  
		Size: 76.4 MB (76383996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1c25d33ce1787d01794b79d1ee12fb0e867081e54f72f84e30f8373293f194f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82bcb435d76429d5e7cbd5b550a8d4201cc87704743e052400bb8079afe47d8`

```dockerfile
```

-	Layers:
	-	`sha256:1219cce0e1fa4b3bacc24eafb44c1c90558bf76b4f59977415de0d8df937b971`  
		Last Modified: Thu, 25 Sep 2025 03:48:02 GMT  
		Size: 5.2 MB (5196743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7a207abb491fd0b74a0c17e26dc8b01b84b6434997f54d8702a859b0efd9603`  
		Last Modified: Thu, 25 Sep 2025 03:48:03 GMT  
		Size: 8.7 KB (8652 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a09ae53174b1cf5684c732af5aa3af7ad430c8c1fb6eb5f5f3659435c39fe276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128498447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70df13112d788f106219e9c21410e39346b52959a9935a2cd0d385b645456cff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844b1b861bc8411c3353350538c3313c5f8292f60f5712603d193d5c167628b6`  
		Last Modified: Thu, 25 Sep 2025 09:04:18 GMT  
		Size: 75.6 MB (75599009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cb34496f250d8dedd91ac7017b9cdef67a6f76080aafe47afe02b329bdd8b5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f751520de09263f96199ab6fc1a89ec707d5ebebb3ddcd676cac0485e30e58`

```dockerfile
```

-	Layers:
	-	`sha256:ba027dd107ebd15b6bb7e69c9f9a4f0c11b0dd0dc31eaa2b6be2191f60d314e0`  
		Last Modified: Thu, 25 Sep 2025 03:48:07 GMT  
		Size: 5.2 MB (5196361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8ad97cd19297443c74002147aab26c47addeebc9eb647b2b9602448547a57a`  
		Last Modified: Thu, 25 Sep 2025 03:48:08 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
