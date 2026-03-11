## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:8254e09f9ce9c58a391d7069d96087a7fb7d656f64d920872439ad89f1be3069
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5eed4d48da9b649782d29cd3497d48da7d223a46f57b1e20a3b9a5a2d77e1734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144003510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf9a41a7a6afb2f15bee124a767497471c01f41952f165c7dec8d8be97f0507`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:13 GMT
ARG version=21.0.10.7-1
# Wed, 11 Mar 2026 18:34:13 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:13 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:13 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383186ccd66fa65eaadaeb7299eddf3d01ca4308c9d98b5fabd2121c611359ca`  
		Last Modified: Wed, 11 Mar 2026 18:34:30 GMT  
		Size: 90.0 MB (89970420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2510b985fbb9f764527ff9aca73fea2e42addb2d1434014d73c22943d2830174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd791b54104bee016df58c3a7a70745c35a24e0ade767bc179be780ce5555e1`

```dockerfile
```

-	Layers:
	-	`sha256:af093d1d385c4572e34da529192c5b503f9837b1c77153c4044cde6fe26bf66b`  
		Last Modified: Wed, 11 Mar 2026 18:34:28 GMT  
		Size: 5.2 MB (5210021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df395e7229fb2b5e30bac5bb7dec9dc95a6cb377cd81021ad2c93c59290c2f9c`  
		Last Modified: Wed, 11 Mar 2026 18:34:28 GMT  
		Size: 8.9 KB (8891 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:de46b9f7489e42bfbb6762f5bda92691c53ac5103762e097ae0054d645e3b364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142054627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f756d08fd8c5c672dfe1337c2a78d1add1a9635e30cbaa751bb214e582a05ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:33:57 GMT
ARG version=21.0.10.7-1
# Wed, 11 Mar 2026 18:33:57 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:33:57 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:33:57 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:33:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecec3de22f32a75f200598e935ba97cf44ddc453f00fbd8ed6f356201c833b7`  
		Last Modified: Wed, 11 Mar 2026 18:34:21 GMT  
		Size: 89.1 MB (89113252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e6bd7e5820ae0afef6c90e01ad2852c86a02eb3c9fce6765689905a96af27434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4c5818900d18d249aabd9b12c055f6ad516204b5382cbc4e6e2da7f36f185b`

```dockerfile
```

-	Layers:
	-	`sha256:faeaa6a15d40e3f9d905141b333eaaaadc5fccd430847988ed7e61c9ed946014`  
		Last Modified: Wed, 11 Mar 2026 18:34:15 GMT  
		Size: 5.2 MB (5208814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:904d5621478ad0c3d4b140f40b57fdf017c625e8e3d5f81767ebf7fa03f46f2b`  
		Last Modified: Wed, 11 Mar 2026 18:34:13 GMT  
		Size: 9.0 KB (8970 bytes)  
		MIME: application/vnd.in-toto+json
