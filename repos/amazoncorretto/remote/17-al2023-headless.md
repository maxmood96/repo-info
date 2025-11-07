## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:9b34f54113acfc7c3338e1c0a7685e9ef0cf211325bd9bdee69acec3b16dee75
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d3cbcc28a67ab796b6d644d0271a807e551e0b04644e6c27ae3050b0a8c539ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136385370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebf80102ead02d6c584f90b70a6ab26b6a7ee34fb79ab9e2e013f2af1a4c6a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:00 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 23:12:00 GMT
ARG package_version=1
# Thu, 06 Nov 2025 23:12:00 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:00 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1abe117f8d583c00254ab166ab020d5ffa837605c28472db8d8ec121e24b1f`  
		Last Modified: Thu, 06 Nov 2025 23:12:41 GMT  
		Size: 82.4 MB (82384867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e07cf815a75214a919f3164babd4cfa2d7178b523d2517f98111619248c17519
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad26b7d9a2dedef67fd9060cdff44ad7e0f9e8910ae699ee98a3fb0edf208643`

```dockerfile
```

-	Layers:
	-	`sha256:fea45fd54e31349e66c8b766b7cd63f5e88fb46df633fa9a3f724f7a8c76f03f`  
		Last Modified: Fri, 07 Nov 2025 01:49:32 GMT  
		Size: 5.2 MB (5182896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a5bd7b3c3c9e37f5ee577b70832ba3059b53f5d25985405d0eb6ed5c0bd5ef`  
		Last Modified: Fri, 07 Nov 2025 01:49:33 GMT  
		Size: 8.7 KB (8713 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:70484f74b839222e338d133b53b84bdc6340de3610be1e1a6ec1471c0a2ddfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134703391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea46facf25c72056876724ad06db4e6600f8182d337b726452c9749740f6343b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:23 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 22:13:23 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:13:23 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:13:23 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd908448f982aafca0074633bc23b4ea0b0d4b4d7e450734ca6f342dbd713686`  
		Last Modified: Thu, 06 Nov 2025 22:14:09 GMT  
		Size: 81.8 MB (81801707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f1ac5400d192b68bf130fcd748e6511a0549e2e9527589c6df1fab094e6710ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e986f0263f45bae4fa2abc83435a03f9bcf22ea42d9983f57043c53e9fe1b820`

```dockerfile
```

-	Layers:
	-	`sha256:b6001bd16c2bfb38c4147e409baedd27948fd74ea3626d48f143f2e00ef0ca23`  
		Last Modified: Fri, 07 Nov 2025 01:49:38 GMT  
		Size: 5.2 MB (5181684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fdf8dd7f3da0527ba1a06fc609db519a81df500b258b279c8c36061bbe83352`  
		Last Modified: Fri, 07 Nov 2025 01:49:39 GMT  
		Size: 8.8 KB (8793 bytes)  
		MIME: application/vnd.in-toto+json
