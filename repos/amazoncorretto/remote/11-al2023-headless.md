## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:67505ead48269871c5cc8ed057fad010f4f2a3cd7ca643f158bf6eb106b631b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:786584b45adef8b2b843c6376f03f197565b443f8edd6bb795facf08706982d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128100215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a6f0881506ed1a718e12b8b18d023b9bed40c27dfe3e2573e5e57178eae4a6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Mar 2023 18:20:25 GMT
COPY dir:c497d3c24209ef7d81f9c5abb7b10467dadda6adcaf860be5c03baaf83b5e43b in / 
# Tue, 28 Mar 2023 18:20:26 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 18:21:52 GMT
ARG version=11.0.19.7-1
# Thu, 20 Apr 2023 18:22:33 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Apr 2023 18:22:33 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 18:22:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ee5c3b4d09bc9dd7590b7480cb385347f445a9fa73056b912cc9ed67ce54d0ce`  
		Last Modified: Fri, 24 Mar 2023 03:10:39 GMT  
		Size: 52.3 MB (52255843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d2595dbacde6539b617efd3fd7de6eb42dc6d60b4d301a7b66bb29770c2ffc`  
		Last Modified: Thu, 20 Apr 2023 18:32:05 GMT  
		Size: 75.8 MB (75844372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:79fbc7c6acc121e6f4124c8957813660c3afeec405f0ecf699f45e1ed0c17eda
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126305175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a86070532184a9040e8fc67361d67f2f819e80ae4b2122b50254fd3c065411`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Mar 2023 18:39:52 GMT
COPY dir:0b162ee66bcb569c55f662aaca3ee7fff9bf5a498748208a280de7797569e5dc in / 
# Tue, 28 Mar 2023 18:39:53 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 17:41:13 GMT
ARG version=11.0.19.7-1
# Thu, 20 Apr 2023 17:41:47 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Apr 2023 17:41:48 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:41:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3a410071be52fec7335cb666804896319a1ac81ef15af4c0f1302ffe8834b63f`  
		Last Modified: Fri, 24 Mar 2023 03:10:43 GMT  
		Size: 51.3 MB (51297211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c11aca305e35358449c787e3bb7344730083549cfc6ed2d3eb7962e2502491`  
		Last Modified: Thu, 20 Apr 2023 17:50:54 GMT  
		Size: 75.0 MB (75007964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
