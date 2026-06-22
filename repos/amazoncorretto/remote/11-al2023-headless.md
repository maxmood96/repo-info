## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:54eded67f926eb9f9b5e329195588bfade1856263b0e49fe962e0e61aeb3cbb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eea28be5d3b8e3a774ebc0fd7e20cc0d9925cfb9c572a68d338f92c83ebdc9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130632369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79eb2123ad44b9213544a25f75ad39cf923d0e9dd15e8355feb472b495066542`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:04:07 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:04:07 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:04:07 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:04:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9ddfe77a89531e6ce7ffd1d71ec21567c05c5ccc876589e3bfc688f5ae954a`  
		Last Modified: Mon, 22 Jun 2026 18:04:24 GMT  
		Size: 76.1 MB (76058186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ff16a61246584b8e8d174c24f1ba72a9ce4e8457f66ffd2994e484e6b6c52b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47f14bbd75ab014fffe5bbb03fd524ccfad052c78a6c7d2fc455b86fbd2eeb4`

```dockerfile
```

-	Layers:
	-	`sha256:9d73b5472266511aae8cc0fbcbd87c515b1d7275e2d0598836c29fa5a899d218`  
		Last Modified: Mon, 22 Jun 2026 18:04:22 GMT  
		Size: 5.2 MB (5209029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31890904597a1a78c2f9d596a78c11897bc60638e61945c1bb47c4f3e0f0c284`  
		Last Modified: Mon, 22 Jun 2026 18:04:22 GMT  
		Size: 8.8 KB (8783 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:eb6c0f6149f9ae3034e47a8010adc4bf72a871867cb467240447c7f9f277dea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128756962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9a1735675e5fdc59fbf2d7fe3f5cfd3a0875893884709b39db16373bbe9055c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:14:09 GMT
ARG version=11.0.31.11-1
# Mon, 22 Jun 2026 18:14:09 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:14:09 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:14:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185eaa0768437220e6d9333e33112262e5ad90a919182de0b6bc2390028c32a3`  
		Last Modified: Mon, 22 Jun 2026 18:14:27 GMT  
		Size: 75.3 MB (75306276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0c8b78e2bfcec1ba35b178f75b6b4780d87754b89538b9f72249c657b574faf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3d5837bed067a4017c4bed55c5c0c025047c032d1afadde11822e7704db4b0`

```dockerfile
```

-	Layers:
	-	`sha256:d88ab6c6bc93db42e61307443b38650f26b2c21409b7a8e4c1a455f5e16b8170`  
		Last Modified: Mon, 22 Jun 2026 18:14:24 GMT  
		Size: 5.2 MB (5208647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba88acc556cc30204f15599afd5e1b5b2554062e285fa7502a2600a7ff721ae3`  
		Last Modified: Mon, 22 Jun 2026 18:14:24 GMT  
		Size: 8.9 KB (8863 bytes)  
		MIME: application/vnd.in-toto+json
