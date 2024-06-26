## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:f71608a7b4e93a64e8e64a4671d7a3453a34a5fa5c16709d05761ea7d8edd820
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5baa9aa86f4746efca831fe1c29beb00d22dcf3c46cd2f6d89c439bf62d04a0a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134736834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85ed29a0a689e7193ee54df5e5050843d4f44d0e64d895f22d63050960bcb7d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:20:08 GMT
COPY dir:1a64694c076f4e5a1aad0a3ea24080e6520840f532ade5fd6b4f5f6a7cd949b9 in / 
# Thu, 20 Jun 2024 17:20:09 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 17:47:51 GMT
ARG version=17.0.11.9-1
# Thu, 20 Jun 2024 17:47:51 GMT
ARG package_version=1
# Thu, 20 Jun 2024 17:48:37 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 17:48:37 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 17:48:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:25f617ca51f740a5a4c48d42acec404063181c588237158652d8a28cdd8abea7`  
		Last Modified: Tue, 11 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767550af23632607eaaaad6f3bab3d7a689ea429f5129d04c7424f3b879f1fb9`  
		Last Modified: Thu, 20 Jun 2024 18:22:08 GMT  
		Size: 82.4 MB (82417321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:21284c35793a84859e049ed3787818a4f027415f12aec6ff01ac815b31f1eee5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133146567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479a06a19674a81d78f2780cc76f7859b2576c580e43951724413cb19db3654e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 20 Jun 2024 17:39:29 GMT
COPY dir:0c9326c957c0b22895e223bbba2686fb8615da2af32396db3026daf720546255 in / 
# Thu, 20 Jun 2024 17:39:30 GMT
CMD ["/bin/bash"]
# Thu, 20 Jun 2024 18:24:05 GMT
ARG version=17.0.11.9-1
# Thu, 20 Jun 2024 18:24:05 GMT
ARG package_version=1
# Thu, 20 Jun 2024 18:24:42 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Jun 2024 18:24:43 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jun 2024 18:24:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:15e2a4581bb8a27d0865d7375063b10dc543dbcfa6a288911a297aaf754984d9`  
		Last Modified: Tue, 11 Jun 2024 02:05:34 GMT  
		Size: 51.4 MB (51406731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9291e40bec54fc5df0ff2fcbd5baf2133045c19ecd32077f9c339cc63bffe07a`  
		Last Modified: Wed, 26 Jun 2024 16:50:03 GMT  
		Size: 81.7 MB (81739836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
