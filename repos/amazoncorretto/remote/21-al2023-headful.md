## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:530d69229f8df7b6c6b10271bc17c984363c286744379eae8dd4a7e5a56db4f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a2470970222e5fdd7e322887409465762f5cb38c9a91a2e4d09f119d91783b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142604256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d0ff29ac3b12fe0e34c3fea1d10b73b74275c50f2dadb0d6dbb4f088e2b980`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:c47c958e2656696575f4e9010ed0d3c34019fe304ebbcf04a253156a78a5b402`  
		Last Modified: Fri, 09 Aug 2024 20:49:36 GMT  
		Size: 90.3 MB (90286353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fa38343f71bc87584071276278e257e987c9fabaf73596564276b7b94d1ebf2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f59bbf8354294cd21a902d12a4a03d20e9f0a2aa90a089ae73e7d6405878c0a5`

```dockerfile
```

-	Layers:
	-	`sha256:681ca23ad64105a8430d8d7692b369939502d053065eb8bc7bda78db930cd5cd`  
		Last Modified: Fri, 09 Aug 2024 20:49:35 GMT  
		Size: 5.2 MB (5211202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda771a0fb43950367eecdea26c09300f6a1e6fb1596fc60154ae4b57c9a34f2`  
		Last Modified: Fri, 09 Aug 2024 20:49:35 GMT  
		Size: 8.9 KB (8893 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c832debfccb6cc3f7a41c138b9b8a3dd9bf478b049680ef48f3cd1afaa9b2671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.8 MB (140754228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331eed29b7802bc7982016ff17735ae7a6acb645c9b3d212ddb83d3234e6bae5`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:af75135ae2bcb204d3424605d578f60133d664f4068ec9d44703196e31fb3b38`  
		Last Modified: Fri, 02 Aug 2024 05:50:18 GMT  
		Size: 89.4 MB (89352216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4c7107e97e462ef86bce98cf35a75a5fb20d35fff5377cc19b183227a991bce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02af8255749463ea7d76b5e32f4aa3475eee58e4a9698f1ffad69c5f78d8c0d`

```dockerfile
```

-	Layers:
	-	`sha256:e3505b74fcb4719a0cb59667ecb9a143946f4655be904ac7b87bc27b015052f6`  
		Last Modified: Fri, 02 Aug 2024 05:50:16 GMT  
		Size: 5.2 MB (5209947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a9c4af94c0b385c539935c501f01d6873b91edce574f9dbd131d4c9f08c665`  
		Last Modified: Fri, 02 Aug 2024 05:50:15 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.in-toto+json
