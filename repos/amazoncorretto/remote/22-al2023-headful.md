## `amazoncorretto:22-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:1567b97296f7c6153280685996d6031dbc033dc0431ea70f34cfd70274db20bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fd7f553298325f85c4da8674aceaa6b61e211c73333e872e6a3e6565a7974eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141368426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf23894902d1eeda2976c0a99dd1bfa2d11b34747c47fcda3dfc4a60d5340bf`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:cb6230c89c15ad3884b7222b06322338ef758165e0b4068d1270a3c8141a3e43`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 52.3 MB (52313926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84564361fece98359ab358097733a3664aa96d1a6a705d1a8b9034568829d412`  
		Last Modified: Fri, 02 Aug 2024 14:55:50 GMT  
		Size: 89.1 MB (89054500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4e2f2e5b5d54fed345f55c5701f11554753bd6ffd3c44cfbde78b0e297f4611a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b1b16c63dd69b31a85d5b1eb2fdc07bc367a36ac1f7d709f2614e4c78f733a`

```dockerfile
```

-	Layers:
	-	`sha256:e992dad7fdc0a49f47d05c3d58ed7952d99cfc8dcb6d42e18b5580d8de6a37bb`  
		Last Modified: Fri, 02 Aug 2024 14:55:48 GMT  
		Size: 5.2 MB (5212294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e82b48e4a87d12785701cf9906bc08735aecff54a53f964dc1e43a0d86c50917`  
		Last Modified: Fri, 02 Aug 2024 14:55:47 GMT  
		Size: 9.2 KB (9214 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2f363af6678faed595786c3cfcb5bc605535595feb8e09ac3e4defe044e670e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139424080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb82e2f993d68325c7bb337b30f437d215b2651970f8a00f073ea53df1646ee`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e62da9c23f6c2bc63e5e53d65284a42bd5bdb7038cd9e7f242023ff4ff0a18`  
		Last Modified: Fri, 02 Aug 2024 05:53:02 GMT  
		Size: 88.0 MB (88022068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e60bfd0aff791e732793aa567a97d71eafca80770586f5a5ae63b9b4da3a0858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d487d50071c5970df7b6e471d5be6335906aaac7fc72e477e3ab788099563f`

```dockerfile
```

-	Layers:
	-	`sha256:8d37fb0056bdce8a04144f83033946bc7ebc0b57863efc09e3a1aeb2051ed307`  
		Last Modified: Fri, 02 Aug 2024 05:53:00 GMT  
		Size: 5.2 MB (5210281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6ed6324189ebf47e9eb3f2edfce532fc7fac6125482d0f87fb96a6f1717182`  
		Last Modified: Fri, 02 Aug 2024 05:52:59 GMT  
		Size: 9.6 KB (9588 bytes)  
		MIME: application/vnd.in-toto+json
