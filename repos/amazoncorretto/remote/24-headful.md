## `amazoncorretto:24-headful`

```console
$ docker pull amazoncorretto@sha256:b70b3d08eb86424c1aa3ae4597d6dd0d122868af35d9e1631be476bfc99c231b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f8de50d3b98b86af54436f7dd70e23a5f0b20cf3052a31308322b5af8706b4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157036440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7f885689a0121469e47c126f4aaf673e68e09169713ad9e68bcb55b39002dd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:0727f841555e830a24054117b5d53ecc18438e2e82fc78dd3cc766ca6bb76cab`  
		Last Modified: Wed, 10 Sep 2025 02:33:49 GMT  
		Size: 53.9 MB (53875706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a3aa51e81722b9115a8f583ad3eaf73e94b28016d4f517f04fe8b052f54001`  
		Last Modified: Fri, 12 Sep 2025 01:11:09 GMT  
		Size: 103.2 MB (103160734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:56dd48bf8c402f709089269f4417e994733229c9b8c845132076bef1b52cb1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2bcdbba6851df6a13173a223ce838d4050811ff4018390be38c36f10ff8c1b`

```dockerfile
```

-	Layers:
	-	`sha256:0bebfdb592ac7f68b62950c7fe26c530bb4eac5c82d9777873a5e5130f7ac95e`  
		Last Modified: Fri, 12 Sep 2025 03:50:59 GMT  
		Size: 5.2 MB (5220128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0157f54b1beda5957539e26bc2f1f4d9840cf1bf8d7727f3ca6ff223b1ba67a6`  
		Last Modified: Fri, 12 Sep 2025 03:50:59 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e99290d9dc06ecd317933eec3f139d9b3c5312f25bac895ee99361f03de20c52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.9 MB (154949498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d071bf76641619181006639fe55949dd47c1ba4e7e34b74035d0321c44b6dc9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a2133584a03a0323a461f4ba1900a168268d3305d6206a4e0a210c92b146e94a`  
		Last Modified: Wed, 10 Sep 2025 02:34:05 GMT  
		Size: 52.8 MB (52775111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1379e6be857b72f81b0d482fa414d8b85fd8805fd772aa29c23a3d3c10ad7221`  
		Last Modified: Fri, 12 Sep 2025 01:12:57 GMT  
		Size: 102.2 MB (102174387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1c7a1374daf98c7394d4b49a906f71538d351ebaddcd5ec4f0819aa91527a562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad03895004c758018ca1e1fc78f05bb21e1631fc72f3551268cd826301ce77b`

```dockerfile
```

-	Layers:
	-	`sha256:c507f729709ad0d9f8afbedb6523c21c8e987b5764a270bbeb0e1f0427dffdf5`  
		Last Modified: Fri, 12 Sep 2025 03:51:05 GMT  
		Size: 5.2 MB (5218942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea576a1645abb9e3def311bce2d441e21d492bfd69ccd0865a01e9c6b1c670ce`  
		Last Modified: Fri, 12 Sep 2025 03:51:06 GMT  
		Size: 9.3 KB (9347 bytes)  
		MIME: application/vnd.in-toto+json
