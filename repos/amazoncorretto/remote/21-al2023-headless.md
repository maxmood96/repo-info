## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:df385fc70385c58ebba40e6c79e4fe62fc8269886c00448786afc451e66c55c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:57cf27438e66a36e0a03bd4d259dab6ecf9d12b8c3c0423ce08982e736fd7b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143280570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8807b89962b27607dfdb882dc08d6ef9cc654ba54177f6d7a105e4bf0095af8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Wed, 05 Nov 2025 01:06:31 GMT
ARG version=21.0.9.11-1
# Wed, 05 Nov 2025 01:06:31 GMT
ARG package_version=1
# Wed, 05 Nov 2025 01:06:31 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 05 Nov 2025 01:06:31 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:06:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c8279c6a5375bf3c24951c0e5a17bdbc61742811bcdba80fcf6bdb19163a13`  
		Last Modified: Wed, 05 Nov 2025 01:07:05 GMT  
		Size: 89.3 MB (89279335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:90a243d2a15d9b3e4861baf60aa6bfa66cfa425492960ab71c2b0ccb22dd49fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2cd7cb77e19fed3bc7f60e8ef4fa19980be2bbd057150bc20b19c755246c91`

```dockerfile
```

-	Layers:
	-	`sha256:9097f55ab17cb0da61ff99532cd23dcafebdbf65fee2022dfdb86cd8971df49c`  
		Last Modified: Wed, 05 Nov 2025 04:48:15 GMT  
		Size: 5.2 MB (5184514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa82b9fe7086e4588d0d096abc386fd8287b43f985170ebf97a7b62947a259db`  
		Last Modified: Wed, 05 Nov 2025 04:48:15 GMT  
		Size: 8.7 KB (8706 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:75818b47a0bfb9c0fb263a0c650a9312673482b709a7f1377a85908cbb9cf03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141296741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c795f50859b616a0b38ecd8340ac55328391d2e43980355453bba3ee078ec53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:14:11 GMT
ARG version=21.0.9.11-1
# Tue, 04 Nov 2025 23:14:11 GMT
ARG package_version=1
# Tue, 04 Nov 2025 23:14:11 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Nov 2025 23:14:11 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:14:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295bb38d897f9d6e75a24d97bbce9b32d3409cf0b346763a4ed10e3c7bc2022b`  
		Last Modified: Tue, 04 Nov 2025 23:15:03 GMT  
		Size: 88.4 MB (88394890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8505286449cb67792b31fffade3302d2171631569ca6c4ab0dde4caa27d9f903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfa05282a4e62f2749228977450313e2481b1064709f29a9be8e7ca5c75b29f`

```dockerfile
```

-	Layers:
	-	`sha256:34c23114744221dbfebf8664a437a266bf95b19b5d7425d5506af3d0665a5455`  
		Last Modified: Wed, 05 Nov 2025 01:48:27 GMT  
		Size: 5.2 MB (5183304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcaa43a162b1a316b98406be1ca49199347275a7487a4ad2547212bdd0bbf00d`  
		Last Modified: Wed, 05 Nov 2025 01:48:30 GMT  
		Size: 8.8 KB (8786 bytes)  
		MIME: application/vnd.in-toto+json
