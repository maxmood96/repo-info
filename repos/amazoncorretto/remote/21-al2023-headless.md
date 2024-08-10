## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:5dc97631b13cee2b9129d6967b722f65decd221350c8900917477b8d7dfc78b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9b74e227b7ee6c1f7e06ef4f4aa172300e56e63be6d0f58636e2af3c5ac6dd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141901061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f790733db81cf4bb8da1c3ee11528a8aa3d73a2a982fbbb42dfbbc189c1900d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:36abe32954e208232b374495838288731226df866aaad9291ccd46166b252416`  
		Last Modified: Wed, 07 Aug 2024 02:04:15 GMT  
		Size: 52.3 MB (52317903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2888bb54d8028843ebdf448070a3e12bbfad0ee68b12082ab4c2552fbc1dc016`  
		Last Modified: Fri, 09 Aug 2024 20:49:31 GMT  
		Size: 89.6 MB (89583158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cd2082de072b98997e82b0ff493d77bf8ce63004c31e68a04e24ac6353ec7e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7159157080c17425b1d8fe053a3c1cc4d97041390e0f571842fcb5d72f1e0f14`

```dockerfile
```

-	Layers:
	-	`sha256:9ee331adf05d3aa0f7b07b82a50cdbe2bc063ce36199663e72d827388c520bd0`  
		Last Modified: Fri, 09 Aug 2024 20:49:30 GMT  
		Size: 5.2 MB (5186087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f629ece030d6b8b1840f104d62754ff7a5c99b181321344e1596abb0a0f5b64f`  
		Last Modified: Fri, 09 Aug 2024 20:49:30 GMT  
		Size: 8.7 KB (8713 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dae236934d77e46948525c27cad50f1ade59df70cdcaab19a5cef446f61868c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140028083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6600b37db71c462ff18d01131ba81f2b4d33b3bc068e618d47b1e49b46ba77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32156763bbbf2a7fdf3b06cf7c795e7c33ede46d8dc51823a91fca275d8b2d5c`  
		Last Modified: Fri, 02 Aug 2024 05:49:30 GMT  
		Size: 88.6 MB (88626071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fc1d52550ccffdb4c39e47fd8b9fb176d8fb7f719dd13abd1a563f8edf5068d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98413fa5872ef2925f6320d4e8744af16a16e47fa208e5ccfbd449f3bb0db21e`

```dockerfile
```

-	Layers:
	-	`sha256:da22e2e24da4e43eb7a32562b54b6d0a284c3b7add4a9cc9f8755c181ba489fb`  
		Last Modified: Fri, 02 Aug 2024 05:49:28 GMT  
		Size: 5.2 MB (5184829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36a63ee970b272a95a313dd4fa3b3448308e9579245cd55caa4bf01b77df2f8`  
		Last Modified: Fri, 02 Aug 2024 05:49:28 GMT  
		Size: 9.1 KB (9075 bytes)  
		MIME: application/vnd.in-toto+json
