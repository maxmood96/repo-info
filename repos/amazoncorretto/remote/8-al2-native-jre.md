## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:0749c7fdfcc315ccb0e46a736a787fef988a642ca4d0252aef974cc5481e9a05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0b50b8ab77b9c9f7c8adb2d866dede75818a3c9e0932cafc3367abc22d279e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172087004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daa2bd9158740c63927a8e3893019c25e71de5b5bc78a56176d1b8b073b9eae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:57 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:57 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:48:00 GMT
ARG version=1.8.0_482.b08-1
# Mon, 13 Apr 2026 22:48:00 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 13 Apr 2026 22:48:00 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:48:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f38ed577df6548675a5fe473b549803609aaac4808f8ab11bd38ac4d838e3e`  
		Last Modified: Mon, 13 Apr 2026 22:48:21 GMT  
		Size: 109.1 MB (109131738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b78e21eabb4aa0bfd1f7e120d94f2ff7476a943c1b5a46b3bb7a509764bb33ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4323137c4902fa52ae076fbe75898e38837ef244be9c1e70eae9284c883a5414`

```dockerfile
```

-	Layers:
	-	`sha256:c0e2204297640a3671e5d2ed5a350ccc1f6ee4598d791a4f0f89dfc1230160e5`  
		Last Modified: Mon, 13 Apr 2026 22:48:18 GMT  
		Size: 7.5 MB (7504229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fde5fdbf8574fb3bcb8aa3dd68372399224b449479fb98ec8fa4f25b635e3be`  
		Last Modified: Mon, 13 Apr 2026 22:48:18 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3f4865233124bbadec35650e103090f3ef29ba429e8a2668af3c62abec47f77b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.8 MB (117771925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9460519113b33a1c931ae907209dbe6c11a68f5484d5af73824a262a85f23889`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:22:09 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:22:09 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:10:34 GMT
ARG version=1.8.0_482.b08-1
# Mon, 13 Apr 2026 23:10:34 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 13 Apr 2026 23:10:34 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:10:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c630bb7364ee12d296fbb10dfb65904050fcace2fc66fb0cc4813d46c496ab`  
		Last Modified: Mon, 13 Apr 2026 23:10:48 GMT  
		Size: 53.0 MB (52968950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5f15abbbb298a78755536949029dcd38e500448355372675a7922d88dbd37c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67239a0d6f8e812a7665db013d0a429156c2c717cfe8fd8b22e45e72a9643603`

```dockerfile
```

-	Layers:
	-	`sha256:e2071d773ba49cfc889a47629155eceb30faeb58ec4c641d19053d55331d8fc3`  
		Last Modified: Mon, 13 Apr 2026 23:10:47 GMT  
		Size: 5.6 MB (5618988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73bad84fc7e217549a8d58c9ab618169fbebfa3bd922230997b7449c212e172d`  
		Last Modified: Mon, 13 Apr 2026 23:10:47 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.in-toto+json
