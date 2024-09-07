## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:c277eae174cf61ef08c35cf98e87800c9f3cd69c8d8e8825159685d432c0fb14
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:623678bbd218d3ba4ef48e48103dd7e840833e34da2a8dd91ce86e6106fc0363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142610501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569517d5315684c5f072e4347e836396054a0732c36ba58e06ef83f7e3a67fc8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f9dd052e142d6bbee3556a17548362b00b044603d859f7ff1a81d3ef6d64bd6e`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 52.3 MB (52325199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ffc18e7b17d01368d7cf74eee8b726ff03220d50f66d7b3f76b1f7c2c11902`  
		Last Modified: Sat, 07 Sep 2024 01:06:04 GMT  
		Size: 90.3 MB (90285302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:888c1a638b464cb59b3740a51daf7418fa92fe2ac26f77528c3a8e21b4ac04c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92598f5642e0187ffefaf8a36588198b01712f7c9d5b0a97368a0301d80d2ac8`

```dockerfile
```

-	Layers:
	-	`sha256:9129da09357ce497901050226deb072c3429d8377e1b60af662da2e22179c66c`  
		Last Modified: Sat, 07 Sep 2024 01:06:02 GMT  
		Size: 5.2 MB (5211290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41e7b79f338c93b7afeea31a4d49acb9e23288cdff2531b55e200736f107882f`  
		Last Modified: Sat, 07 Sep 2024 01:06:01 GMT  
		Size: 8.9 KB (8893 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f29cd672913f036f56424055bee0df86f306661f1106ec52155e95b4bf028aa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140762731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da9d4f5694f6b529440d621b6eb70d17b2618e76c0dbbb63514ec363f6dba2d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:875f26d62c6d0f5a935b0c8548e8375f2a9b98d7669bf434dcd5b36e2114348a`  
		Last Modified: Tue, 20 Aug 2024 01:54:55 GMT  
		Size: 51.4 MB (51426298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42a92b6f45893209caffc3d0266e31b43b61350d42ee52d358e53471603f17d`  
		Last Modified: Fri, 23 Aug 2024 02:36:15 GMT  
		Size: 89.3 MB (89336433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3eb80e4e57f5a89ed86e2040dcbe29b2bbe203dc4789ea1e3e45cb603abd5f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14bc5df2d4b9f332f7698a676d8d8e31332a2c6a60e5bb993aa5b4cb001a17c`

```dockerfile
```

-	Layers:
	-	`sha256:abe098cbb33e189fa175a1865b576799d9bf981848c1cdd5496b18a425b21a4f`  
		Last Modified: Fri, 23 Aug 2024 02:36:13 GMT  
		Size: 5.2 MB (5210081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6c820439992a87c9c334a3374863b2bddc3b191ac99215e64399af16643800d`  
		Last Modified: Fri, 23 Aug 2024 02:36:13 GMT  
		Size: 9.3 KB (9254 bytes)  
		MIME: application/vnd.in-toto+json
