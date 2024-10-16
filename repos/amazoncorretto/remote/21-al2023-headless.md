## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4d73efc90d945cfb8bc2920d330ec0bcda7ce4109ac7147c5a5eaca4c69ff823
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0f11f535c3f1348aed81229f17d23c9d7d1d50683a686771872d8af6d452aad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141226081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53fc9531011365305d75d2b3ce331e187f781fb9a8f1a05d1b849e779021778b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:49 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b70254d58d211707233d28837c74ed2204ea8300430b7827e57901003251129`  
		Last Modified: Wed, 16 Oct 2024 17:57:44 GMT  
		Size: 88.9 MB (88900776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:728ddd12c85e9fa628fbdc039c6844a9a398de7cdec8ddaecd09495a0e21ed1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91292b3fb0dcb6e23becb48b0ae0d32f64c203d5f3b7c36eb18635955de3d6ff`

```dockerfile
```

-	Layers:
	-	`sha256:49999f627bbe9db426784887e6e113ff72cd83e14dd240860c11c7c79034359c`  
		Last Modified: Wed, 16 Oct 2024 17:57:41 GMT  
		Size: 5.2 MB (5186192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:088651a075771de8e58cd32097df7f15c19dda06658a25f02eb299a75c84ce8e`  
		Last Modified: Wed, 16 Oct 2024 17:57:41 GMT  
		Size: 8.8 KB (8753 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3fe4f7fb028f9a1fc919d0216ad6ecb364cff73bc50eca4c8e46e414da99965d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139383672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18d40a522cd0cfc50a8933acaecb6626f618d4b6460800fa3354021b6fc70b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:52 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:52 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b87362a34d915674fb8e37ee736d0e621f1ca0eace2e3853bbae6f3c70dd48`  
		Last Modified: Wed, 16 Oct 2024 18:34:39 GMT  
		Size: 88.0 MB (87957308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:42c13d4c24971b081db70364c562426d0a3868ffd5c62a3ce1f077a5f217e1f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63239b72fe9e6d92837d77ad36028a31859520c1f4f24d1f574fdf31a1eb2047`

```dockerfile
```

-	Layers:
	-	`sha256:ed672c94357ee40c11568e7b5cc56134c0799ca215e296ca9b540eaecba91c65`  
		Last Modified: Wed, 16 Oct 2024 18:34:38 GMT  
		Size: 5.2 MB (5184980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc1495f3e98b2c2f88bb91e66845acaa8c62289cd0d0592b437cd4b84a665ed6`  
		Last Modified: Wed, 16 Oct 2024 18:34:37 GMT  
		Size: 8.8 KB (8833 bytes)  
		MIME: application/vnd.in-toto+json
