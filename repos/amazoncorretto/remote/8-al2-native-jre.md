## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:43929eedf7e12344e3939222b2676df3d5b77a76648b258792020696e5475978
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4a236baace6265671a682bbd5c9d00a6eabf1afd98e79b9871bccc72f9748a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172081004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fd7694c7a552ccd0269edde5ad01d7d9e6cce88fd2c21f73895897e2fa7277`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:32:49 GMT
ARG version=1.8.0_492.b09-1
# Wed, 22 Apr 2026 21:32:49 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 22 Apr 2026 21:32:49 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567eecb1307a5743a8d7a0464a0b9bb29bab6b506435a9059f11ea3a1426759f`  
		Last Modified: Wed, 22 Apr 2026 21:33:11 GMT  
		Size: 109.1 MB (109125738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:279b86330a4594e7e00460377acd8acdcf42a0d8f8f9bb2c0cd2d5903b8ae36b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d68c3d0438f7f80f18f93df1f41c3a0bce15ec753108865d4aa853e96d500a`

```dockerfile
```

-	Layers:
	-	`sha256:6a6afff3d19f437be8ffd5ed2175c882aa6d35c6bf7aee7e2e2e1a89a8645f27`  
		Last Modified: Wed, 22 Apr 2026 21:33:08 GMT  
		Size: 7.5 MB (7504229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1199b7e5390a0b2162523985e8496e3fa28ae0ff41ecac728c418c874c5fbb17`  
		Last Modified: Wed, 22 Apr 2026 21:33:08 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d2e3c1cc5ea653dd38880f6c91d1b2b4e5768ff12e0123b007b6ea3a8d09f945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117770773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048164f1073aa57580624b209746912a300d6c23fb7a50d3cadf7385e73d4b34`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:32:45 GMT
ARG version=1.8.0_492.b09-1
# Wed, 22 Apr 2026 21:32:45 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 22 Apr 2026 21:32:45 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a905e33ce008ca4584ab4502d7f245eb8d6dd0671fab44216079c34d5107e15e`  
		Last Modified: Wed, 22 Apr 2026 21:32:59 GMT  
		Size: 53.0 MB (52967798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1d3b1c4e423a0d7a687f6e560185cb5c3558b6dd50b206038afbbcc81814b7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b6f94c796aedb6efd71fe717868c9c5bcc927162e9bfaf7872a7e898ecb8f4`

```dockerfile
```

-	Layers:
	-	`sha256:2ab1ceb035db365e9dee5b9824d164127cf14d03952c2282da4e6dada3a1c9fc`  
		Last Modified: Wed, 22 Apr 2026 21:32:58 GMT  
		Size: 5.6 MB (5618988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19923f68284287b34e437c7b95b243502cb740a3b431527492109a9735a34a08`  
		Last Modified: Wed, 22 Apr 2026 21:32:58 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.in-toto+json
