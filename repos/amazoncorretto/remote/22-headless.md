## `amazoncorretto:22-headless`

```console
$ docker pull amazoncorretto@sha256:1842b50f4f6be81e560aabb0b52d824685f24c4d77210290128021d88e69b9f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fb5cc0afa48bb423b129950da74a1246effbd677d1d4d723fa6b9e16f7e05df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140653256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3323a77a21e95689fd24106a9ab73936667c36a108e8fd224aed3d6c866ce03`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:36abe32954e208232b374495838288731226df866aaad9291ccd46166b252416`  
		Last Modified: Wed, 07 Aug 2024 02:04:15 GMT  
		Size: 52.3 MB (52317903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4639b5f3bb2c63bf61e8e5ff8d070e00edd7ea59884b64fe8ab8c29f5436b27e`  
		Last Modified: Fri, 09 Aug 2024 20:49:32 GMT  
		Size: 88.3 MB (88335353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:735a3c273069a498824db31f4890c46409bd04558aa1306ed88efa6848ce2ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494227d41e35d8c331a4e1f2a62e130f04d5652a88fa729232e5d73284e11196`

```dockerfile
```

-	Layers:
	-	`sha256:6aa45f4a80ac36f7e308e52337630d553a1aa26fe62deafd8254f45c7bba92a2`  
		Last Modified: Fri, 09 Aug 2024 20:49:31 GMT  
		Size: 5.2 MB (5187227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6498315039e64ae765e682bccb5efa39a2ebaad614ad59069d50c5fe3a70c879`  
		Last Modified: Fri, 09 Aug 2024 20:49:31 GMT  
		Size: 9.0 KB (9035 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:20464dd44cf1c6a8536ff8b2c07d02ff60a9b809088b0a9e97702d1ba25090b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138698923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff63c130094af90f790bdef47c6b818613762e40a9f81946e0b6debe3b05a99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:6dc418e3f016a388470ba66be212f100f862b0633543844e880b17590526cce0`  
		Last Modified: Wed, 07 Aug 2024 03:04:12 GMT  
		Size: 51.4 MB (51409634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b291b7a2b5652d1a7c9f5b20cc3904679e5c990ad000c29d2a97a3b095593056`  
		Last Modified: Fri, 09 Aug 2024 20:58:57 GMT  
		Size: 87.3 MB (87289289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dc0ce88971e53253c02ef7449702c2dd0eae10d1b7cf1ccba87eb3894ba8d205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58dd31f9e7d2f863f5aeda6590480d72b75da371b555b12d1c703695b1bd6ccc`

```dockerfile
```

-	Layers:
	-	`sha256:16cb56d9236a0436144b613171cec5a7b4930f772a49ab4684e3acc961d47b8f`  
		Last Modified: Fri, 09 Aug 2024 20:58:55 GMT  
		Size: 5.2 MB (5185211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d733d03360ee88b154158bed4cda79dd2536901e7b220d3964e2fdbc81128aba`  
		Last Modified: Fri, 09 Aug 2024 20:58:55 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
