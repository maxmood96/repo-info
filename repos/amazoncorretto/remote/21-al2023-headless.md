## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:8fdd39bc7591f064aeb01f5cb5c34ddd4a8686985220231718de88cbbab2034b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d4cd9339a8b8eec0453a13e1212e393f65651043167eb400d442ab5e9c536661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143262448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b6abd7bae71c9bb4bf5104b92934aac1aa8b13d660f484da235816bf15ceec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:01:10 GMT
ARG version=21.0.10.7-1
# Wed, 21 Jan 2026 19:01:10 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:01:10 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:01:10 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2dcc44ee6bf835463d5392a2e6d2c4a03f38a32af5699772934832602b9674`  
		Last Modified: Wed, 21 Jan 2026 19:01:27 GMT  
		Size: 89.2 MB (89241244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e8bb6c85168aa3db927370658921895749c2575de1909cb3a70ede370232b8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bff3a428862c59b6d0d10a0777ea98e3140d904f38aa638f42e180dfeb1b9ba`

```dockerfile
```

-	Layers:
	-	`sha256:a4e3ef37986eb2026a69ecb1a7f238997fb71aaeda0fc24c6730f36e3d9c45e2`  
		Last Modified: Wed, 21 Jan 2026 19:51:57 GMT  
		Size: 5.2 MB (5184522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddc649f1143c8523465ba0c372c0092a94f237b54d35b2035f36abadd5a43f1d`  
		Last Modified: Wed, 21 Jan 2026 19:52:00 GMT  
		Size: 8.7 KB (8708 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:00e0e30a31eb7a3cc69772b38b58d3399bcd5bb12dcced551ca808d9d84da769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141288963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2230fde31183a8934861c3f63e1bfe2a06a807891084ca52f36d113c242db8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:01:33 GMT
ARG version=21.0.10.7-1
# Wed, 21 Jan 2026 19:01:33 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:01:33 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:01:33 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:36 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3124ded65c5a0540fe7441403dc539a001fc2b9741b353b0af9194d1a904ca5b`  
		Last Modified: Wed, 21 Jan 2026 19:01:52 GMT  
		Size: 88.4 MB (88374606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9ce5e64c5913b974094364f169620662c789189d157596e2320c9aa4d06fc3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38307accdb1c4e165d6665df77e46d5a9c0c30024a703bb5a556dc86d2b45ffa`

```dockerfile
```

-	Layers:
	-	`sha256:f40a822eea464faba3570ba64d26a3db28507977f674d8036cd8be2cb16797e4`  
		Last Modified: Wed, 21 Jan 2026 19:01:50 GMT  
		Size: 5.2 MB (5183312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:130bd538253eed8406c43717d0904395fd3ec20e8b639ee0e6cf6937c6b8dc27`  
		Last Modified: Wed, 21 Jan 2026 19:52:07 GMT  
		Size: 8.8 KB (8787 bytes)  
		MIME: application/vnd.in-toto+json
