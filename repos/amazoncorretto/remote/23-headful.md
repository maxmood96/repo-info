## `amazoncorretto:23-headful`

```console
$ docker pull amazoncorretto@sha256:5d8bd2f2a6c0a7df3af4e262ee80f5e0dec0ff5a43514bd9352cea43555aeb81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9b67ef8457c1d37a5c88235a290a36b2740330485aa3fa0193b4ad950119e02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146092665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5de36daf4a3ead4ae408d9d549c9f936f0ff9b0d986ca246173f2b12915a0c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136c5bebff8e3ab99932a3a4263a0358893dd00c91d56148a35dade65b510c97`  
		Last Modified: Tue, 08 Oct 2024 00:01:15 GMT  
		Size: 93.8 MB (93767360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a78346ae5b72e6f9cf61316d794bceefe7587adea811d8b3a3964ddf8f675039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5ba91cfb2ad31405cf6918b0d296d036e1860b6b6dad59a3dca51ff3cba2af`

```dockerfile
```

-	Layers:
	-	`sha256:2188b0c4ce0acdac5cc57593dc407e4bdab69553cfb7d143bf7c2ebb5469aa7f`  
		Last Modified: Tue, 08 Oct 2024 00:01:11 GMT  
		Size: 5.2 MB (5214126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93e7aeb1d5ccf253b4ab0d03cbaba309ee9163ef1b58a47a27763611584be485`  
		Last Modified: Tue, 08 Oct 2024 00:01:11 GMT  
		Size: 9.2 KB (9225 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:997776b9aa88c931af0b4f3d8b0fd032b549a8ba6aab2131d2b75332723cdcb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144134258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d235dae62e9ad660ff9c379ea0457c443c66c4e463bc3cab0d07ec78e354c2e7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ca7e5292fa23b45b78f048449112a29ce9dc2cef3c1eee0994ec0f9bdaf2dd`  
		Last Modified: Tue, 24 Sep 2024 02:50:52 GMT  
		Size: 92.7 MB (92708266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3220d75fb0df13fa80f4bc8b707f33cf55c84547a512f05816dcb1c524bfbff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082baee0e64cd87066d15540082c5a3868341baced6d2fa8269f4d31324f4e22`

```dockerfile
```

-	Layers:
	-	`sha256:061d10294c39db5aeb2f7c3391b8c498b5c032a80dbfca4eef1aa64a8a992019`  
		Last Modified: Tue, 24 Sep 2024 02:50:50 GMT  
		Size: 5.2 MB (5212102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21d57bd34687b1081f736000b8e90e5a10c4954d855b0e5fad72012f10d8289d`  
		Last Modified: Tue, 24 Sep 2024 02:50:49 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json
