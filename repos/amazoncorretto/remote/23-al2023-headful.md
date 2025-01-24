## `amazoncorretto:23-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:3854b1ffc01245e4040b0cf46cc6bf34c780ecdd358adaa86f6c5eeaed7d7ca9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:01bf7a4f0cece728f36bf4b3542fc14f0789b53c98bf4fa5628331e249e7e183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (147001055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26cbe6b68a2e774c370f7e2c97167cf6858329ea7627abefb6c406a07662e763`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2025 23:01:33 GMT
COPY /rootfs/ / # buildkit
# Thu, 09 Jan 2025 23:01:33 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=23.0.2.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef86dca54b314270c90c6332cb5c5f7ff821dd755be71b91ed026b6daf51138`  
		Last Modified: Thu, 23 Jan 2025 18:28:11 GMT  
		Size: 93.9 MB (93850580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f2c682fc2f4a931a6d287715eab570365f73de7171be2fac5fbd1da356a7fdb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661038674908e9112aef3ae5b614e9c6546c279414c01b9795d78435119ea0f8`

```dockerfile
```

-	Layers:
	-	`sha256:451f832ddcaaeef8b2f06cc1f8fa3eac8e130d5648122eff5a7cb451da12b824`  
		Last Modified: Thu, 23 Jan 2025 18:28:04 GMT  
		Size: 5.2 MB (5209108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18c0d1db95c6038df709cfaadcb7997331762c8ebfc9cc9a3b34c0c78b9076e`  
		Last Modified: Thu, 23 Jan 2025 18:28:04 GMT  
		Size: 9.2 KB (9248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:afa1674cd570647cce00a91bccb39089206a7e77bcd56fbb54a56602c2df0367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145134050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebd31ef581247254a69ecb3bb621c0fb38bb0c33a8eec3cbc14bd37d1caa9a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2025 23:01:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 09 Jan 2025 23:01:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=23.0.2.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c26f528be964f57b9ede0e6a5f497757f1bcde3a4dd2393158c54de614fceb`  
		Last Modified: Thu, 23 Jan 2025 18:56:24 GMT  
		Size: 92.9 MB (92865854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:815cffdebd844d43ce6f879bb490d278f835db658aa589d68ee12640019639c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be937c22ee68e878470d57e7f446c23071c6aa1800386fb0a5a9b97c4ce42a88`

```dockerfile
```

-	Layers:
	-	`sha256:9eed25258d3a988a69ddd61e9bc8d3e62601a954ce9e1023a521182c2ee08c19`  
		Last Modified: Thu, 23 Jan 2025 18:56:22 GMT  
		Size: 5.2 MB (5207100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15adc0f85f92233924cfe31107862b9bb944361339c4403c5b48c711ca8eec44`  
		Last Modified: Thu, 23 Jan 2025 18:56:22 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json
