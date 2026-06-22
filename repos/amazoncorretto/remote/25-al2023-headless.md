## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:0bb088911afe4777e29d9e13441775f66a71eca9fbf616a00896e49d90646410
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:63d51599fc348ed385dffb14c53cac97025d2ef8bec86e23bc5347e92b226132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158295065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6716cd9563f48bda78752af32510055bb19c68a903dc2368d0502022bb77b796`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:13 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:05:13 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:13 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:13 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9974fd3d56e34147d91d6d7eac3a96d72252b2a617a11ede6a55423061558e`  
		Last Modified: Mon, 22 Jun 2026 18:05:35 GMT  
		Size: 103.7 MB (103720882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:89fa216a7a8da83db2c1ec4deb2af6424a6828ddacc80c5a14b55b75d119a5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c8fc226704bb856656d80ad179d5814fcdfade5be9d498318d71a7b340e661`

```dockerfile
```

-	Layers:
	-	`sha256:16c95849826e7f9f3bdb56b5371be91c0feaa6ca58a44a36acc94891fdc44ca0`  
		Last Modified: Mon, 22 Jun 2026 18:05:31 GMT  
		Size: 5.2 MB (5207808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdec6e6b0928426702108f19824d9ff36c1d837227467438edfd61ae1391c891`  
		Last Modified: Mon, 22 Jun 2026 18:05:31 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:96a3aeed7ccc3fd1dbf23f07bdee4bf40f5119641204cb8f7e32a6fd356f9068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.1 MB (156103475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc8fa636d7d5cc0d601ece72d5f8714c86915d17724b164bb08428966af96df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:46 GMT
ARG version=25.0.3.9-1
# Mon, 22 Jun 2026 18:15:46 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:46 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:46 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49871b341ca9ff45aa5b4e8309da20374f1825d259c42f0614b0d76791b483f9`  
		Last Modified: Mon, 22 Jun 2026 18:16:13 GMT  
		Size: 102.7 MB (102652789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dddfd53e481a41b85004dac961de2b6d63abc566de3f818b781455a64908e003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e8e2b8a6c9f345aad82152566dfa8fedd709a5b1556adec73c762ac66e2efb`

```dockerfile
```

-	Layers:
	-	`sha256:b38d729483e79ed9679c8b99330945133092b83eec5d9725563892f338cfd24e`  
		Last Modified: Mon, 22 Jun 2026 18:16:10 GMT  
		Size: 5.2 MB (5206620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13f984fbc4883f2b42eb3a066d9fc62c8a137d78f7a4c1f39aeca13ca6466aaf`  
		Last Modified: Mon, 22 Jun 2026 18:16:10 GMT  
		Size: 9.3 KB (9290 bytes)  
		MIME: application/vnd.in-toto+json
