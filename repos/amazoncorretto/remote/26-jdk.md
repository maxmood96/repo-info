## `amazoncorretto:26-jdk`

```console
$ docker pull amazoncorretto@sha256:a246774eaa249c020893dc0eeacbfc3cfeeada938dd41d94086ba489afee1ead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2eaa2d9f576c25c364d60c69bdf7b97dde084a842c7efea9884b05108ecb3458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.5 MB (247483998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3546a162b0a6f0146bc0d5483a002d8c2d7e0232b139bc67014a0a9fe1854a49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 22:59:10 GMT
ARG version=26.0.0.35-2
# Tue, 17 Mar 2026 22:59:10 GMT
ARG package_version=1
# Tue, 17 Mar 2026 22:59:10 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 17 Mar 2026 22:59:10 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:59:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fadb71013635672ae33c1fd1d4b1cc5cb891f0e21625c872f41e1558e3b5dd`  
		Last Modified: Tue, 17 Mar 2026 22:59:35 GMT  
		Size: 193.5 MB (193450908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a98345f2e14c1431d45d1ce08e4a3ad86efd49e830debb82c46631713de62bd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac418a9df760826e44f2da471e8cb942a744d9eb81fbf3ce4c44bea09c96cfc7`

```dockerfile
```

-	Layers:
	-	`sha256:d0505e2949ce13d29803bfd0ca7010ce85af7678ce2bb54a4ffb225f9011a90b`  
		Last Modified: Tue, 17 Mar 2026 22:59:31 GMT  
		Size: 5.3 MB (5326370 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ced84c642069d9957f496c739999fcab4bae4b0087d02b4cdc656fd7fae57118`  
		Last Modified: Tue, 17 Mar 2026 22:59:30 GMT  
		Size: 10.5 KB (10510 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1862882d24fa3c29a0aa12d61c571b46342dc0c5e7470823d142327717af9b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244215542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f42bcd57798e1c714e90ce2282980ffac27dc1e848be3eb1bfb8d0b63b006f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 22:59:05 GMT
ARG version=26.0.0.35-2
# Tue, 17 Mar 2026 22:59:05 GMT
ARG package_version=1
# Tue, 17 Mar 2026 22:59:05 GMT
# ARGS: version=26.0.0.35-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-26-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-26-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-26-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 17 Mar 2026 22:59:05 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:59:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94aac8ebdc12d0c969682c9776de97101dd0e74ef22d894237a7dbf995c0c9ab`  
		Last Modified: Tue, 17 Mar 2026 22:59:30 GMT  
		Size: 191.3 MB (191274167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d2104b3b11304f02828b768b217831f56c13cad76149f81a524b46cc6665ddff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bbe7a97537c73321ba86e2b99e45795e0e57aab62675c5a8231d1cae8cfad1`

```dockerfile
```

-	Layers:
	-	`sha256:e12b287620e68cac41bea1fccea93863b5304d1c743b1a643c37e225a8f8d56d`  
		Last Modified: Tue, 17 Mar 2026 22:59:27 GMT  
		Size: 5.3 MB (5325346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68eecfe9044a253ec2d9cacd9476abfc2b5e8a1c0092ad6f6999a0eaefa2d61c`  
		Last Modified: Tue, 17 Mar 2026 22:59:26 GMT  
		Size: 10.6 KB (10638 bytes)  
		MIME: application/vnd.in-toto+json
