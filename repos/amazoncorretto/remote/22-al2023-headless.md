## `amazoncorretto:22-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:c329b2b3fdb4002859a46e81d3945e46dce8a23a5a5da9de83f89e9fc0dc0d02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:46b9fca3019b94ea7555ca14783fe1309bffbbf23bce656f2af45540b1849106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140663514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65d80ea3ccbe5ed5c5c60f6f1d733eb9148fe31baff98ca6479ea416a76e2c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=22.0.2.9-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c56236f9382f1b5938bce45fdb924bbc107ef936df014ce0cbd86d78f266c28`  
		Last Modified: Tue, 08 Oct 2024 00:00:45 GMT  
		Size: 88.3 MB (88338209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e3ebbd6ee811c08122d3b6b05636c6b3099249d51762b97cf736aeb8bc330db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c05e1fd9946d2ff9de810e98af00472fdf5291dbdc5bc0b66644720a607787`

```dockerfile
```

-	Layers:
	-	`sha256:46ac2dab980dab1964d87d47b8802efa75a863d936f97ed54a3f5d2167e70a63`  
		Last Modified: Tue, 08 Oct 2024 00:00:43 GMT  
		Size: 5.2 MB (5187328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01fd14f482f13f11f4e184824ad68cdba56549565354aa24965928bc6fa20ea5`  
		Last Modified: Tue, 08 Oct 2024 00:00:43 GMT  
		Size: 9.0 KB (9041 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e4a0e96cde720be407cbbe5f85668c87c1d33db97b13e68e302ed165c349fd3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b59a62ea3f5608e84d0bb2d24dc5c6e81eb5d53146e0488314983d9ae36c9bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=22.0.2.9-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a29ab6cecb9bae4229378a478f8a20bdcc01a8eb19dda5f3ec0b6f823da6ea`  
		Last Modified: Tue, 08 Oct 2024 02:15:33 GMT  
		Size: 87.3 MB (87290067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:576a14d61ffdfe0a2f0a660ab0f7eb94362224187a925bc09fa16c463cedb091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6137c9971805787aabe95e2b96e3035890cebb959fbb91830ffcafb84390e0a5`

```dockerfile
```

-	Layers:
	-	`sha256:290cab24f93672563fc5ffce6d62dd727f98140a95ff9c66f9d60258617d34b7`  
		Last Modified: Tue, 08 Oct 2024 02:15:31 GMT  
		Size: 5.2 MB (5185312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d71e68d91e70386bc36ccdd347b9e2b2a49736b04b3bdb5c0ed409485104dad7`  
		Last Modified: Tue, 08 Oct 2024 02:15:30 GMT  
		Size: 9.1 KB (9135 bytes)  
		MIME: application/vnd.in-toto+json
