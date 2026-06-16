## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:90bc007fe414016187d4c1cbf02622f07c4d12a690b2a23aa04be1b8b75b5847
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f1fc12eb337145920a22c4d18265bb76bab31a79f94dc774cdb19b75b495e568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144663973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490a7e522b1f27060345e9f3c57f231ef2fe538f08e1e268efd4236b3cf11873`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:05 GMT
ARG version=21.0.11.10-1
# Tue, 16 Jun 2026 01:16:05 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:16:05 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:16:05 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde4467a7e2e6858e309811d52f6954d3e952bb300577fd800c211f9dbd7b925`  
		Last Modified: Tue, 16 Jun 2026 01:16:22 GMT  
		Size: 90.1 MB (90092817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c4851e30e541aeb93750af3981c22dad9eb92e59979f7d4b5008f930339ab126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5226273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc39f16c24eac2378a80ddb16a55b773970e30c9c6e0fe3b67eb3dd9f6eae8d4`

```dockerfile
```

-	Layers:
	-	`sha256:e74354a945532e0d5122627d2d235e00e4be4f5533e6af63b15cb2afe98afa28`  
		Last Modified: Tue, 16 Jun 2026 01:16:20 GMT  
		Size: 5.2 MB (5217220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc84fc99a8d853b24721932de26fa8745134da3d6819a068912bedb1d578225b`  
		Last Modified: Tue, 16 Jun 2026 01:16:19 GMT  
		Size: 9.1 KB (9053 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:19684d3dd84f46d748b40d28f14a734f8d82383d9102a2d93d2787aefc4c3afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142688197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e01d9cc95d03e6651ac3fea70e59d6e26fb4fc4028cbf9f4c8680d929148d2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:17:09 GMT
ARG version=21.0.11.10-1
# Tue, 16 Jun 2026 01:17:09 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:17:09 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:17:09 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:17:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec72d111aaeb64287626c6c6dd5ebceb81657ecef3c96f2d279024edf19c4f7`  
		Last Modified: Tue, 16 Jun 2026 01:17:29 GMT  
		Size: 89.2 MB (89230370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:455ecdad865ee9e185fc014d5640348979207354795b64b344b84c5abe3b7777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cc088adbf6bef37703fb7f0ba1ad2d88821e256872b517533490bf16a5cf33`

```dockerfile
```

-	Layers:
	-	`sha256:cb1d94ce181245adf3b5f03814168385c03c3bd2f79ab1930e2b7c1d53666e21`  
		Last Modified: Tue, 16 Jun 2026 01:17:26 GMT  
		Size: 5.2 MB (5216014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77ec9a00fc9923131a179ec330c421b75ea0089a13fa14a4dd2fa92f48873fbb`  
		Last Modified: Tue, 16 Jun 2026 01:17:25 GMT  
		Size: 9.1 KB (9131 bytes)  
		MIME: application/vnd.in-toto+json
