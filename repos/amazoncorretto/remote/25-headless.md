## `amazoncorretto:25-headless`

```console
$ docker pull amazoncorretto@sha256:8aae8add870d08ea755eda939d20b35ad63d824a357e99ee4b2eb0ae9fbeef36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9edef8ff04c30c4b2904d2e6db715e41fcdb6df699bebb13aec3340dcc2bcfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158180813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b376d2733843cd4f22068b853ee7fa5edd469ff4a2dc2985938f7040af412d98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:49:40 GMT
ARG version=25.0.2.10-1
# Mon, 13 Apr 2026 22:49:40 GMT
ARG package_version=1
# Mon, 13 Apr 2026 22:49:40 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:49:40 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:49:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ed3c2ad2d594b26ee23f10ffecb5d15d4209488f6aba7680ba27873cae7137`  
		Last Modified: Mon, 13 Apr 2026 22:50:00 GMT  
		Size: 103.6 MB (103609559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b95479f4e0a006be6ebcb4bedbc8ea9c6bef231914b42a180d0f01b857e9efe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5210434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982aff1a34a412441cf657ccfe60a822d1e1c58aa3107b5b8226ecc91c88bd44`

```dockerfile
```

-	Layers:
	-	`sha256:75646c660c2eaf8d42723f8200be5a8963bb89ea3f3767e2c0416c5c4198ffb6`  
		Last Modified: Mon, 13 Apr 2026 22:49:58 GMT  
		Size: 5.2 MB (5201235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3f5789fbc4c90ca1af1e6b5672f0bc38240433ff1c11efd1fb5669b4072f254`  
		Last Modified: Mon, 13 Apr 2026 22:49:57 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:20408086ae3818e331e6034e684541827a24636b8dbb576ebfba9e7fdc619e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155972579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afff93806dd43af09e85e8f62242e9262b6fea5dacc0113a60e0fa985d1a8b23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:12:17 GMT
ARG version=25.0.2.10-1
# Mon, 13 Apr 2026 23:12:17 GMT
ARG package_version=1
# Mon, 13 Apr 2026 23:12:17 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:12:17 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:12:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8191acae07c7b01fcae5515cf06c057cc1de713f754cf5bc80f54097887a53`  
		Last Modified: Mon, 13 Apr 2026 23:12:38 GMT  
		Size: 102.5 MB (102529840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cd5fd6ed08d06c5b7071454a811ef56a6c6ab72073c533dd7a273a72624b8c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3ca3f0d14a5835b3565a08bcfd126067f9195bb4fb679d7d9621d87def1d38`

```dockerfile
```

-	Layers:
	-	`sha256:795b16468e794790fc431c09e4726476046083c8053566900cdf81cdd06c51c2`  
		Last Modified: Mon, 13 Apr 2026 23:12:36 GMT  
		Size: 5.2 MB (5200046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0af6749a66302ccf21d24399375206171f4959c0fbf4c4b7ea436498debd884d`  
		Last Modified: Mon, 13 Apr 2026 23:12:36 GMT  
		Size: 9.3 KB (9292 bytes)  
		MIME: application/vnd.in-toto+json
