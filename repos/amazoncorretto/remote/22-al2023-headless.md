## `amazoncorretto:22-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:9963bb2e74258c0f03e137e7dc39d2671505381e6bf415a3f035fa0234a1762e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3d54a1f042eb73c3de012ec8cc963ad0d22f09c56bff308b99a5bfa63d071623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140918983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0562986f42c1d4d8a6f111e099b47324fe539286b47ce4866c8e57464a1cf15c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:1c9e0f4db95e1ae683b8f16b1ecfc5d8693ad4e5e379a2386e2870f38383c7d8 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=22.0.1.8-1
# Tue, 16 Apr 2024 21:21:40 GMT
ARG package_version=1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=22.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:860904071dc658e37de73aa1556e7badfb13bef4747965ea3bd1049e8ff87dcd`  
		Last Modified: Thu, 04 Jul 2024 00:20:13 GMT  
		Size: 52.3 MB (52319623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1610ae186940ba4c9b19cedfcd3ff51fcf238a577963f6161bf59dcfd114461`  
		Last Modified: Fri, 05 Jul 2024 19:56:52 GMT  
		Size: 88.6 MB (88599360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:28a2baac78a9c1f86127402ac07b363af13faaeecf79232213afdfb8721d9b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5169295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7231591c1c512263e9d65177999849bcfbd46d37f20aeb72adfede5e68c0aa9`

```dockerfile
```

-	Layers:
	-	`sha256:5ab2b74356633e0f0689d103827cbd58edd64785cc2755e8aa2081b3a2352ea8`  
		Last Modified: Fri, 05 Jul 2024 19:56:50 GMT  
		Size: 5.2 MB (5160453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0406abb4776942aec705a8561bfd82d371126bc63f2a537908af0a7bfe484cb0`  
		Last Modified: Fri, 05 Jul 2024 19:56:49 GMT  
		Size: 8.8 KB (8842 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b5e70777ee372e2801e096d3be5f697f264c69bd0f37055e5d3bee0c06109039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138964002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df0418d9292d8907b8609bde1f7a0f252dcc2af8a7dc91d3e4bb04c6af50e56`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:a2f5453af1f2210c7b49fadc5acdaaa335139ac35c64847d2f5879056f91a03d in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=22.0.1.8-1
# Tue, 16 Apr 2024 21:21:40 GMT
ARG package_version=1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=22.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:f95af119e05065dbdff89fbd219657362e32f7ec50d632e28754e75b5a13806e`  
		Last Modified: Thu, 04 Jul 2024 00:39:44 GMT  
		Size: 51.4 MB (51407040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2087234458047e61ac85ac73d2630e0dcb723fd400a21ab4930e283fa42c0ad5`  
		Last Modified: Fri, 05 Jul 2024 20:28:57 GMT  
		Size: 87.6 MB (87556962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e2604cc5c73082c5a0843b42a72c71c967345171b42a19f9e176e2e0f1424f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f234dd621d5c6eca3f1582425009bb045392b1ef8ae4e150a101b06aaeb0627`

```dockerfile
```

-	Layers:
	-	`sha256:27419957ed54823761cfec25824375ca338bda45d73f5dcdff97720b38b44ba9`  
		Last Modified: Fri, 05 Jul 2024 20:28:55 GMT  
		Size: 5.2 MB (5158436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7414a3016b86047700fa725cb17cd5d5c4f511f6471e4cfafe31b54d8728f153`  
		Last Modified: Fri, 05 Jul 2024 20:28:54 GMT  
		Size: 9.1 KB (9135 bytes)  
		MIME: application/vnd.in-toto+json
