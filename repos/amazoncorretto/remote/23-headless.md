## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:9325000750f3f0d5b789426e5dff039d54b139c95eb39b170092f968668bcf84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:577c9f31a4f701c9721a1049af9932dbefffbd7c0a62fca09c8aad7b209823bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149141948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832d01e3d267a76a550897698e683463008fbc71f1952e86f90a34a65067fa75`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=23.0.2.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fab98587ce5af52da7f0e96b60eac5766814e8a6b6fb4735afed4558607ab0`  
		Last Modified: Wed, 02 Apr 2025 00:08:15 GMT  
		Size: 93.2 MB (93234895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3fcfc097636fb88e59609cea14e43b3fa8419e0541d770e81ac5329278a3c9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db04276baae1bb8c1946ab84e859832b88df4a3b05395539c090562592fed1a`

```dockerfile
```

-	Layers:
	-	`sha256:6c498cc16ae5d297b888f67bc67ef5050d7b857734729682a9b51ad67fdf4565`  
		Last Modified: Wed, 02 Apr 2025 00:08:14 GMT  
		Size: 5.4 MB (5430218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98b60aff094b157970eedcbba195edfec5ef24bcc760012b68198e23d4a074b8`  
		Last Modified: Wed, 02 Apr 2025 00:08:14 GMT  
		Size: 9.1 KB (9071 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8bfddb7ca25b15a4bf8f812c3b9b1fb52383ed0bcc836201b9991ff3db0c963f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147203259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01645aae975bb7f4db32f3394666a471ea407f2d12dce1e4fc897785298970bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=23.0.2.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86bd8377f64fce15e095503ce6f16c7dc4af8cec150c3fc700520d6c098ef6a`  
		Last Modified: Wed, 02 Apr 2025 00:36:35 GMT  
		Size: 92.2 MB (92242250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2203c0feb716158841b701fb451b2e6c76f9f483e41b8e0e1b91011946b3a84c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5437371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af96935a59a495edebcd1e721e610a255a9e211e80736404c3b112c9a674a502`

```dockerfile
```

-	Layers:
	-	`sha256:2beb0f771060b02950e864ef6b0f876b3ae75a25bed6915df1349cddbe678be4`  
		Last Modified: Wed, 02 Apr 2025 00:36:32 GMT  
		Size: 5.4 MB (5428207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23848b8066d229b9c1eab85a9a7d7c77db846ae966b7111510896d09b8c2d171`  
		Last Modified: Wed, 02 Apr 2025 00:36:32 GMT  
		Size: 9.2 KB (9164 bytes)  
		MIME: application/vnd.in-toto+json
