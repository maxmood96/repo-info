## `amazoncorretto:24-jdk`

```console
$ docker pull amazoncorretto@sha256:edb5c99cb9bd48dd04c79e6ed9d6c61ce5bffd402d474ae96dc774e34b897fda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c382d66a2fb66bc631e1c08e2282931debaf026e459a2ac089fe2e711c30c4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240306410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106aa3bc72de1355e31e771d1252238dabcfcb4b2eb0ffdf8c14b165ddb8a3fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:76cc64d6a248b04196e7ba8dc6c3e7ff1d81e82f9d332d320529c20ed03cc7f8`  
		Last Modified: Wed, 26 Mar 2025 23:27:10 GMT  
		Size: 53.1 MB (53123289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d5bff2c39fc8dcadb275aea17a37b7a49ca2bf562fc7e2775417994f819f80`  
		Last Modified: Thu, 27 Mar 2025 23:59:07 GMT  
		Size: 187.2 MB (187183121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dc075828f7764817913d0aaa22122a5f3cb2dacf3bf080736a5cf5b0ee7d7243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5315766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad26e39ddaff972962bf175d4798ed643b274d27009123d567d2ddd383a8f25`

```dockerfile
```

-	Layers:
	-	`sha256:6e26e5754b1aef21dd110aae5249f86252d6a206f356c0b749e361527adae53a`  
		Last Modified: Thu, 27 Mar 2025 23:59:03 GMT  
		Size: 5.3 MB (5305527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95c7ab76f888f9af86cc0d12a1c6200f26c72b7ca48a1cd67991709eb82c89f2`  
		Last Modified: Thu, 27 Mar 2025 23:59:03 GMT  
		Size: 10.2 KB (10239 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:db86cfe20c21cc9d1e9a7a891faa1cc6e78f76b1578e29f5b93c1fa46afdb68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237475594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbd73b3164965d7e29f9052b973d4511eb6c23b48313cb10b298618fe39a913`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 07 Mar 2025 18:35:42 GMT
COPY /rootfs/ / # buildkit
# Fri, 07 Mar 2025 18:35:42 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a8ae4757b69337068f85c03c42e1020f67d8e126d57f500162c47221848c93bd`  
		Last Modified: Sat, 08 Mar 2025 02:26:21 GMT  
		Size: 52.2 MB (52245978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6d660cdf4d6b69698db6b3483299194cff733792d5f0e4bc28eda71ae7a6f9`  
		Last Modified: Mon, 24 Mar 2025 17:33:38 GMT  
		Size: 185.2 MB (185229616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:56a1b87a0e36c604b735220865214bc7736187badf25c8e8718b56752bff9354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5314850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1dfcc9e0bf7de5b9d5c89da71ec75bf2ce201850555f3ff162f46efd456545`

```dockerfile
```

-	Layers:
	-	`sha256:6225c3c27c1886b35445978ff9d6b849184237adfa60dd6e7cb79725298d43f9`  
		Last Modified: Mon, 24 Mar 2025 17:33:34 GMT  
		Size: 5.3 MB (5304495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d07116256211ca5c18b93d7688d34ea9c78abd1629065f0b1dbeeb760ce9cf0`  
		Last Modified: Mon, 24 Mar 2025 17:33:33 GMT  
		Size: 10.4 KB (10355 bytes)  
		MIME: application/vnd.in-toto+json
