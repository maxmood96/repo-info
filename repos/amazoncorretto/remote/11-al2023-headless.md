## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:004d687bffd7cc4fd4c7133774fa2f19cc058e256aba6caacbbb7fe517b381fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a2408950cb4f9cfa09b4025856671108ea26afa030dbc9bbeb6f9809519d52b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130630227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c96fee6368706755e0c05ea773553bb57f21c0557d1044120381299a5caa807e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:20 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:20 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:33:20 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69114ee66b4e3b29a4a8abc9434d4b4a0ff9ae0e0db1ae3005e48bfb5b3e83b`  
		Last Modified: Wed, 22 Apr 2026 21:33:36 GMT  
		Size: 76.1 MB (76058973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ecc911c7b09401f4964244020b5929dd80f7d53d408af330de8ef206d50f689e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3aa22d0007229bc9bb4bd9e0bd56b7c2a0f0d748d988c4cf4b7cd1989e353c9`

```dockerfile
```

-	Layers:
	-	`sha256:16f0dcbac5583ee6209f3d8f515b481e2e8c2c31c65e6fe2a79dad604227951c`  
		Last Modified: Wed, 22 Apr 2026 21:33:34 GMT  
		Size: 5.2 MB (5203271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0af54286ec34b137842c93c41820f503d5e6f002eedc659a052d4d04c62cefb4`  
		Last Modified: Wed, 22 Apr 2026 21:33:34 GMT  
		Size: 8.8 KB (8783 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:10da77bcf967111fb9dbae931d7c4bf907a849c626051f412237f97f8184feef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128748776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926cd053e104896fb03fb9f98976c7c1d85d1a58607922b7964872de3b02a04e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:29 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:29 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:33:29 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c93378982c4b20427a1f254de3e90848c80623e4de60c3f1d78aa725c8e887`  
		Last Modified: Wed, 22 Apr 2026 21:33:47 GMT  
		Size: 75.3 MB (75306037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1edfbe94f8f49484e6d4f1a98eb12e5ff1ce14abfe92b661cd1e3a1be1b62099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84eef458b5c9c00f1fdf695d26298fc05059ca9b8fb542b88d20387f2d71ae70`

```dockerfile
```

-	Layers:
	-	`sha256:2ab9059500318d3b97b64897a73441648c477d95ea25a75376ae3dd848e65c79`  
		Last Modified: Wed, 22 Apr 2026 21:33:45 GMT  
		Size: 5.2 MB (5202889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ac1c432b99f28736b89c2bebb2452ad6eeb0aae8f0627e07104258b2f6676ec`  
		Last Modified: Wed, 22 Apr 2026 21:33:45 GMT  
		Size: 8.9 KB (8863 bytes)  
		MIME: application/vnd.in-toto+json
