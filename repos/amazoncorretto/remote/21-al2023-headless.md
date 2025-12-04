## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:90a833bb0394aa6faa8339eff67e19529ff2d0f69801d3098ba9d29db943d0f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8dc7a7a38ef7acae6a7340ebd17b69b80d3342b5c5aed066ae40b9dc08a882c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143215308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d694fbf2c4929b83ae65693c5c421661ab51a9fc015e08d22a2c52da856261`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:24:24 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:24:24 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:24:24 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:24:24 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:24:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf5dabb6652435f98c8a0937b279908b64f1e00e7bbb8a89911ae59c641a13b`  
		Last Modified: Wed, 03 Dec 2025 20:24:54 GMT  
		Size: 89.2 MB (89246287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5e529aa75122395e28e986d01a0ae430cde93d0752fdef77b3d1350b11c7dea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5882aeed1cf9a54ba62779b29a4b9eaa453dfafbb9fdbc84c67a2eceed04a78`

```dockerfile
```

-	Layers:
	-	`sha256:6c0c270c7504a407bcd05355eba79b2fc503121644a444c36d845390709390d4`  
		Last Modified: Wed, 03 Dec 2025 22:50:17 GMT  
		Size: 5.2 MB (5184514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbf676a51c1feaffcb3087518fa9c2ac476198d719c1b81d8bf9b2b3371a2c2`  
		Last Modified: Wed, 03 Dec 2025 22:50:18 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:82f5801338e4d864bb89cd7a95e118f39471bb8e819b0ce2214c6cb3a8aaa87f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141232676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15abcb486f50b9887fd22f8ec25498ed04126add119d8322a55b94f8d550d846`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:22 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:22 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:27:35 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:27:35 GMT
ARG package_version=1
# Wed, 03 Dec 2025 20:27:35 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:27:35 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:27:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee864749fe5034e950e1c2ab80853681d29c4d80f574d2984c5ecd3b84dac60`  
		Last Modified: Wed, 03 Dec 2025 20:28:08 GMT  
		Size: 88.4 MB (88363255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5444bbfb327d88640c551099cb13b60094591665a46f9fc78a30f94f54764209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b2367b8cb3b900d11b4d8c0f7d6b7ed6aa876f3c127215fa3cea88a812f41c`

```dockerfile
```

-	Layers:
	-	`sha256:f2b7bcb5d51c3c667270469f17c67cea609ac2aec0e9655e66495bff9cfdcfb0`  
		Last Modified: Wed, 03 Dec 2025 22:50:23 GMT  
		Size: 5.2 MB (5183304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32a7fd4689b5328fda1931aa2d1779e99dd5cc9f0d2226bfd1d36dd26529470`  
		Last Modified: Wed, 03 Dec 2025 22:50:24 GMT  
		Size: 8.8 KB (8786 bytes)  
		MIME: application/vnd.in-toto+json
