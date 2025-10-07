## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:656532824f5eb2f0cb4d937c5ba0d332d6bc5469eb5327aaa10f2e6dd6db3fdb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:55857d7c6e10beb4f228ac41520424095d603a0bd43c1aa409a10f2e45b553ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158322896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4cde19ed5d9c7109a841fef8aa3a00079762090ca59a95fe43379ea0dc89f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65755d86eb4d437dbfc3ca44d9d977a383fdc09aec72c3ddcad0783476ad7878`  
		Last Modified: Mon, 06 Oct 2025 21:14:35 GMT  
		Size: 104.3 MB (104317765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a74233bfcaca55772d5af70ffb09fca372459e143c2e0dbbefcd94dbb32c8626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fcdfd488d846764e76278590a5ffb1671378fc7eff05480e7e7be9bf2e9796`

```dockerfile
```

-	Layers:
	-	`sha256:08e2e9ad958f85aea7238740754db8cd01af44174767f332e50a86bb9919a6b4`  
		Last Modified: Tue, 07 Oct 2025 00:51:47 GMT  
		Size: 5.2 MB (5220130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc0e273f7218fa20a806f1a4afbf0381bdce0fa73304f75301f0a11237f1ccee`  
		Last Modified: Tue, 07 Oct 2025 00:51:48 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:13b99071146e7804dec9b0225ddbad08480d44ad0c45c7254940e5dad8e54a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156127369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b84e6a0d499a9e36537735bb85aef28fe076cfa19469be0a00f384e2794777`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f3547004dd1833efa319b4e4215d324ea3fe9465064292db8b4f2528f40080`  
		Last Modified: Mon, 06 Oct 2025 21:15:27 GMT  
		Size: 103.2 MB (103236166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9c1bf4a1d213dd6df25f858ab609ecfb81dae70116ce20ddd0054025c3ae6573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3360be16e6e5e5b97b5a468d7e5899edc755022dff9fbea90fa9b7b6cc9ff3`

```dockerfile
```

-	Layers:
	-	`sha256:3f5b859e89890b3f8834a3bddc3e7d490e2a3419cd605a372ca25d2031a61952`  
		Last Modified: Tue, 07 Oct 2025 00:51:54 GMT  
		Size: 5.2 MB (5218944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c790e1b8a9e77f6c7d1da1a33c7636225025ffd3c3e6740bfcd130ae6dc89197`  
		Last Modified: Tue, 07 Oct 2025 00:51:56 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.in-toto+json
