## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:eefee188860dc2cb2f0db38ecaa5c16713cdab0b35edaf6583117145c13b247d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4460d542a073acd1cc7bd3123ea4e558bee62122e90205aea1dc236641945fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129967788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02732b1e9f654b589b1350f1cb4f3da219d3b9001aef047a48b6da99b1a7338b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:17:40 GMT
ARG version=11.0.29.7-1
# Thu, 18 Dec 2025 01:17:40 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:17:40 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:17:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362da6f0caaf2a1ee483a779b593d76c4d492b72c5048d09bbf8c7d302f5acc9`  
		Last Modified: Thu, 18 Dec 2025 01:18:10 GMT  
		Size: 76.0 MB (75979328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:903b7df6a0aeb1fb20402426e82661147e8b65a87a71634b6afb2976edc1131b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30b56930b365b15023c6de06c23f157853c6df800f632547fe9586f9a0acbdd`

```dockerfile
```

-	Layers:
	-	`sha256:c72ce83c5ba84765515aab6b80f5b2b00b2391f24fa421fe6294dd95e1212306`  
		Last Modified: Thu, 18 Dec 2025 04:48:00 GMT  
		Size: 5.2 MB (5196819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12d3fb40cf86e5e0bba266744839f18992c160280cecd4a9dc4a34d78722b52a`  
		Last Modified: Thu, 18 Dec 2025 04:48:01 GMT  
		Size: 8.6 KB (8608 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5bd69fca3921110c3c184798da3520efa0f98b8629989c5c01a21340786b6e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128080860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8daba89164c8e2f1ffcadfe80cb58ec5f2985b457907a9f1fdc846a950788015`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:25:37 GMT
ARG version=11.0.29.7-1
# Thu, 18 Dec 2025 01:25:37 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:25:37 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:25:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c44de42ae7ef93c6a7c6f740e402bc073f49b4603fceb803fc4c444494588`  
		Last Modified: Thu, 18 Dec 2025 01:26:09 GMT  
		Size: 75.2 MB (75207410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:29a1f54561badc3430bcea0a8329c732ae09d22a03bf78ac4f75ccc8c64f626f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa44654113b40b55c954d15125c1bbecd086160797c2a40c085c40f9c1efc151`

```dockerfile
```

-	Layers:
	-	`sha256:fd62fc9431639b5513f0f7867d63672dc8024eddf2f0eb74263bc0852ce8b8a5`  
		Last Modified: Thu, 18 Dec 2025 04:48:06 GMT  
		Size: 5.2 MB (5196437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e770171ad193454a1e439f197ce42b98c1a654582b06c61a9326d968c1775ea`  
		Last Modified: Thu, 18 Dec 2025 04:48:07 GMT  
		Size: 8.7 KB (8689 bytes)  
		MIME: application/vnd.in-toto+json
