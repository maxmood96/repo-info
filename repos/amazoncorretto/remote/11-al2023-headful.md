## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:788cc8a106496151e818f7df7c30ffd7e46df4930db38c40ecc0faa1941ca47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6668b98b1d03ac318cc75121de74ddd05be15e1a643ef8a7fe0d46b13b838709
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.0 MB (128992140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374026287219b45ff6af96bf3e50adc1fca230ead4db8842d49c7017a5ab5804`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:45:33 GMT
COPY dir:3d1c4d9e1017e7de559aec6b3779bdf6668d0e4f73f6af00952a84abd805da43 in / 
# Fri, 12 Jan 2024 21:45:33 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 23:43:28 GMT
ARG version=11.0.22.7-1
# Wed, 17 Jan 2024 23:44:33 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Jan 2024 23:44:34 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:592fcbe9ebcec6e31ad10b3d219e4f61ce8e39180e215fab37ae75bc7ac4c0b7`  
		Last Modified: Tue, 09 Jan 2024 00:19:51 GMT  
		Size: 52.2 MB (52238109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce688d5bc91cd6d807a53bc202a4f540481914f808c0cbfabf0c98328789a7b`  
		Last Modified: Thu, 18 Jan 2024 00:01:25 GMT  
		Size: 76.8 MB (76754031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:36fe0a889258ba7b1928553c4d1b1d7c105cc24b733abec3cd92cb6f013156e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127225210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4bee976942705b2cacbed249e619f77041e17062acd99280b47da4836fefbfb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 12 Jan 2024 21:49:07 GMT
COPY dir:80de4926459dcf07edafbe2044439672e4fed6bf5796881b9953e9ffab3571d8 in / 
# Fri, 12 Jan 2024 21:49:08 GMT
CMD ["/bin/bash"]
# Wed, 17 Jan 2024 23:39:26 GMT
ARG version=11.0.22.7-1
# Wed, 17 Jan 2024 23:40:19 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Jan 2024 23:40:20 GMT
ENV LANG=C.UTF-8
# Wed, 17 Jan 2024 23:40:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:6126164e178e3570337610ef0b171038c4426a730623557513d2ce511166a065`  
		Last Modified: Tue, 09 Jan 2024 02:25:54 GMT  
		Size: 51.3 MB (51303151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d3d65b3bcb40e7e020f1f3c2e63b965588a6b81f5c9fb529a2e4cc3fc90fd2`  
		Last Modified: Wed, 17 Jan 2024 23:54:13 GMT  
		Size: 75.9 MB (75922059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
