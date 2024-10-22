## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:7caf153d71897680951f42169b8cfd023cab985533fd4e45e95b6725ddd44b15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:efdfa1c9532577b4f5fd0a7e0d216cbe6473536186c58035461cfbe1d3e22aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134413666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb427caf4cce8fa251fd72bbcaacbd040152a18806deab5df6cfe34f41eedde4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc9e21fd3c82201d67406b7dc590936071a56dfe72aaef370c7af350abc81b7`  
		Last Modified: Mon, 21 Oct 2024 18:57:00 GMT  
		Size: 82.1 MB (82069834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:afe4f281818d8545b4adbcee01e9377739b3eba7891c5506499f6de17bd3cae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba4cb1137bc9abcd9cf85d35134d55f125e937dd5d192fe8cd286b8da3ee62a`

```dockerfile
```

-	Layers:
	-	`sha256:7ec88a57085489fc657db116a050c73021f5dca3135ad1c40f857f850faf68b0`  
		Last Modified: Mon, 21 Oct 2024 18:56:59 GMT  
		Size: 5.2 MB (5184530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df06d59d471d7284dc9fc29295695e7292488265a50a1ff3fe2950366909fe3`  
		Last Modified: Mon, 21 Oct 2024 18:56:58 GMT  
		Size: 8.8 KB (8756 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d76e05eb65588e11320ccc8d8f279cbc62e511bd34d3cec6efa9883ef4993092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132890675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fba621dc557034c0d5c4486e2f818ba4987742828e5ffdea9e9a084dd40f4f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:923a2071aa1c62af0f57aa46e86e64587ba93da0a38eaf52d228227154730e17`  
		Last Modified: Tue, 15 Oct 2024 02:53:59 GMT  
		Size: 51.4 MB (51424527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900ec2a63a840c0b48325bda6f343709aa28d8e7c2a4464615e2e16e160444bd`  
		Last Modified: Mon, 21 Oct 2024 21:02:13 GMT  
		Size: 81.5 MB (81466148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8907522fbb627380c324ae87523de8d54644a93738017f274886b71a59e69c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9eb611e27258ec04df43f92e6763f51fe548abcbd814c51063b069d5668ea09`

```dockerfile
```

-	Layers:
	-	`sha256:87e0edd587f7403c7c6efe39a068823aa18a324c087602d6257b67e0f30dc681`  
		Last Modified: Mon, 21 Oct 2024 21:02:11 GMT  
		Size: 5.2 MB (5183316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:059c6f1cc402285304d1d55a22e19e6710270be2b17d86bbb9fa48a795099145`  
		Last Modified: Mon, 21 Oct 2024 21:02:11 GMT  
		Size: 8.8 KB (8836 bytes)  
		MIME: application/vnd.in-toto+json
