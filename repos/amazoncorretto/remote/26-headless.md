## `amazoncorretto:26-headless`

```console
$ docker pull amazoncorretto@sha256:c5f9369d3a8eea6e5baceb377d54d86ba61abbacebe221f5c508ae25a456b0d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:49375ab3359f53a2017e15e48891bec2d476c68164d5689b6dd08dbb56199780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160395971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b802d984b395e49b022c54e787ba6cdd9b7535d3fb0fa34beddfdecc5d5d0eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:46 GMT
ARG version=26.0.1.8-1
# Mon, 22 Jun 2026 18:05:46 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:46 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:46 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db150c81298128a4e0337f257880594e9443e20adcc803138e1ef10c895cc6b7`  
		Last Modified: Mon, 22 Jun 2026 18:06:06 GMT  
		Size: 105.8 MB (105821788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:98a14727b0b174d4cdb59c06dc75981d671cb7a8f32115735d9ef3aeb8ce36c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a11592c17a0a1f43ff301119ea9f5751e1883b9cc3b25383a310085627925e2`

```dockerfile
```

-	Layers:
	-	`sha256:fa575c9624cae3a45ac4f0cbec87189e74383c58e8e967cf09bbf22927d81841`  
		Last Modified: Mon, 22 Jun 2026 18:06:03 GMT  
		Size: 5.2 MB (5206166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7809a36002d74f29a6488d7afa23fa415471d63426ffbf04ac7f56db61624684`  
		Last Modified: Mon, 22 Jun 2026 18:06:03 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:01ce6a48ddd8c89e175c6791f54511d9e4e3dceea5c4476b3f36870cf716f2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158160362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0487566d61ef8074e4649e060ac55b4158ea09dcf8f844a975936b631f19286d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:42 GMT
ARG version=26.0.1.8-1
# Mon, 22 Jun 2026 18:15:42 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:42 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:42 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495ac7acdced75524278b8ca3355b588f8dfae365fc3dce78f21eec096b62d00`  
		Last Modified: Mon, 22 Jun 2026 18:16:04 GMT  
		Size: 104.7 MB (104709676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8fb87003804edd7b149b8ec8f17fb2180f66ab9123cc08c9d4221a75bff87306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3140c7a219d4a234fbf04f64543d647c1b4b5e413b7c7991ce191f231c6dc2`

```dockerfile
```

-	Layers:
	-	`sha256:61867f0b57dd354a0c9f74a1256ab5d4c6d8088ce3444ee3d292bd50da32dc14`  
		Last Modified: Mon, 22 Jun 2026 18:16:01 GMT  
		Size: 5.2 MB (5204976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4091b739e9bec528d301e0335979b761ee5b53d965281c064d5580e7d1b853bd`  
		Last Modified: Mon, 22 Jun 2026 18:16:00 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
