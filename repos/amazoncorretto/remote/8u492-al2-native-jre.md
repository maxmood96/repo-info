## `amazoncorretto:8u492-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:69aed3bfffb93e8d00b979b33f27cbd2478a46afd2c0bbc79cb718c8b04438b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:797a7cb250030b0a8cb952eb6f671d3763d572c69aed1e16cca5facc2c96996c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172098790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d45df8f673d7b396f3946f4507e9df9e8c19b93d7aaf7b9b0ac60d01fcbe03ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:40 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:14:29 GMT
ARG version=1.8.0_492.b09-2
# Tue, 16 Jun 2026 01:14:29 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jun 2026 01:14:29 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:14:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fe05e30cd5d4ad167829a8feb195f20a05e8468da40aa6fa5714b48d64de69`  
		Last Modified: Tue, 16 Jun 2026 01:14:51 GMT  
		Size: 109.2 MB (109156840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dc6efde4171965013d795d3117f5351185548de2b5c5babecc6abe9035fe7e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a84a2bf6a2facd1702314712e8d3b874193efda6785c9701cee77b5b60dcdb`

```dockerfile
```

-	Layers:
	-	`sha256:f20102462175025f4a0c9b16637babb9b67738122016d9c90ffad93a91c9e922`  
		Last Modified: Tue, 16 Jun 2026 01:14:49 GMT  
		Size: 7.5 MB (7504229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c489e88743c712dc508a2a807d2bf884b1766e2d3bc7a7c2fddc1e0e913d4c9`  
		Last Modified: Tue, 16 Jun 2026 01:14:48 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2d915f7522ec1d5fdb13b08a618e2d1cff50a3360e474924981045e70e82a8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117740562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78165d72796d62a8289f1963bf8c2d56840471f67ef93ede554c1d59fcdb6f3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:52 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:15:36 GMT
ARG version=1.8.0_492.b09-2
# Tue, 16 Jun 2026 01:15:36 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jun 2026 01:15:36 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:15:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16a0bac00209990ebe28f9925473d617d809224069f219c24c90167a49a29ca`  
		Last Modified: Tue, 16 Jun 2026 01:15:50 GMT  
		Size: 52.9 MB (52949853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:df11d5122696b95b3578b77279dc35f9aa3623a14d81619335cf285c194eaf52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f9c7736a43876ed90ade012618b6e8e298e07cf6cf379b825a892ea4f48ac1`

```dockerfile
```

-	Layers:
	-	`sha256:0ed73659d9c698b771c1244f558c8737f46d6bf8b23322081169c4fe94c767b0`  
		Last Modified: Tue, 16 Jun 2026 01:15:49 GMT  
		Size: 5.6 MB (5618988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec34bdd4d5cef38a9aa24e7d4637fa92fd5066529d7e8d1856aaccccaf2fcbbf`  
		Last Modified: Tue, 16 Jun 2026 01:15:48 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.in-toto+json
