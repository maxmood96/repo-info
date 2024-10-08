## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:47e535c7264d30f3771376efb1533b4a982b2f5215c375179b636caa1312fe1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:92efee0430ea886f1d46de44678e654291971c15c09ae2f4c5d3f0384daae5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145388695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8763793a1c2266766c4c8fe30e1aa59a2b4383ce8a868fa1557d9685a13740`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3b397d1bd5b07c2eefa08dbeafca89c75cc82c67ae554e08cc861312d9f201`  
		Last Modified: Tue, 08 Oct 2024 00:01:25 GMT  
		Size: 93.1 MB (93063390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:84217c954157b5b7432e094c782a9ed45f086719891feaf967a83b9e56e6c16d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3157ac1d699d9c8caea107c091902f52567215bee4250e338e4d0e7390c6f497`

```dockerfile
```

-	Layers:
	-	`sha256:e1b8ca045084482a89d8c348e2ab06fc6498264c4e534de7736891b5eee6afac`  
		Last Modified: Tue, 08 Oct 2024 00:01:23 GMT  
		Size: 5.2 MB (5189011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2cf439110f5a3396235c658858cc9537e16ae30bb0a20d12b53751a55dbcb38`  
		Last Modified: Tue, 08 Oct 2024 00:01:23 GMT  
		Size: 9.0 KB (9044 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:156954a777c19500e57be0e5670a27e42169e39b4182cbbfc6b9c2071746d8f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143409529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e24493a234a0817512c61bb954ab106d656181465ef94649997d18483804089`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab718bdc8edd0c441838457e2189220e3fecc1b79e032fbd9301fd7b7f23a05`  
		Last Modified: Tue, 24 Sep 2024 02:50:03 GMT  
		Size: 92.0 MB (91983537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:44e5a1f7bd028bc6e8de65a2cad213eca967486e1ab1c5cecb6046f5ed066321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799620c11742bfd0a74e6e31bb7100e24d163b30fe317280378e52bdadd0d2ee`

```dockerfile
```

-	Layers:
	-	`sha256:89e39c1d3987ca1891f0559a3450a4f5cd7148a11a3f50c25d7c0fe0e1a367c1`  
		Last Modified: Tue, 24 Sep 2024 02:50:01 GMT  
		Size: 5.2 MB (5186984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e7d1f3f1d587ebbf9f113a8a63e5c1d2c4d6896c675d329c5623478650411d`  
		Last Modified: Tue, 24 Sep 2024 02:50:01 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json
