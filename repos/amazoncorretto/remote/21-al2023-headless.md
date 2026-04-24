## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:46035b45e7a85cd10c120765b6d813f46b6cabc307f5d54e871e1fe227bf7ce9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:902e07cad767d60b8f73256b3639a2fd4fbed0b147442cdca70db885eb5df25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143926190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e67aa540ba8b234d5d749d112d291b4ef5b28bf55814a254da2b832da7f0bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:31 GMT
ARG version=21.0.11.10-1
# Fri, 24 Apr 2026 00:13:31 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:13:31 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:13:31 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82cf391c5b2e4ffb0f5d11ade0e240011253b4d3d7efcd1923ce662c626a5afb`  
		Last Modified: Fri, 24 Apr 2026 00:13:50 GMT  
		Size: 89.4 MB (89356485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fb8c56ef3923d7d50d4902607c10cd7f2f28d31caf8096bb9553a1550ebcef27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf438224bd705ab7dc76eaa1e47c9cdba3fa5ac931298dec18e44b7bca5880e`

```dockerfile
```

-	Layers:
	-	`sha256:f3d25d6ea46b8ca0851813e88be2627c93410a64d4fc4bb1a10b34dcd3c648ea`  
		Last Modified: Fri, 24 Apr 2026 00:13:48 GMT  
		Size: 5.2 MB (5191789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec0be065f6602c2a80b7111417aa761b5a2ce2053adc5d433718688aa1648f9`  
		Last Modified: Fri, 24 Apr 2026 00:13:47 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f6db791fbc144afba50f5d3eea2d0de131c8ab7a775ad3920b75b8b9ece7c825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141943370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e33a4cee6bcfcd7b743bf3dc08056dcdb12aa44073f7557274f531469c8afdeb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:36 GMT
ARG version=21.0.11.10-1
# Fri, 24 Apr 2026 00:13:36 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:13:36 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:13:36 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c53305c1bdc55ba00c04d30dad7b10edfd57096fe3ae63fa887641cb735d7510`  
		Last Modified: Fri, 24 Apr 2026 00:13:55 GMT  
		Size: 88.5 MB (88491117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:17d26755961e194839a99bacb215d1a66568141b35176b4ca20410a4b8658428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5199542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8bc55132f1627c237d641051204a142456633b78f041bcf294713b2e2eab5a`

```dockerfile
```

-	Layers:
	-	`sha256:c41e7806818a38fdab415acb0d5e716b1a6b00fd989dbc488be9cab39c7f220e`  
		Last Modified: Fri, 24 Apr 2026 00:13:53 GMT  
		Size: 5.2 MB (5190580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f0367b84663410a6bd0f11d45d301cd430d84fab853d1f560dd9b07568ae6d`  
		Last Modified: Fri, 24 Apr 2026 00:13:53 GMT  
		Size: 9.0 KB (8962 bytes)  
		MIME: application/vnd.in-toto+json
