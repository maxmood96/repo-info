## `amazoncorretto:8u432-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:bc4b44c984f70a2f4ae0346b67ea4bd29eff195bd47dd141b74582fd58d48e1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d757ca4c830142618965b78d53153d1e82339eb239238f66b1c9d2603fae8317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171781799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98099922f6a528f82baa72890734ab2067179a2e5e7335bb7cb20d5634070a50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:32c87c6464b59c63781462d4129c84f2806c57bdb75e94414a62f13a51d7b113`  
		Last Modified: Thu, 17 Oct 2024 08:34:33 GMT  
		Size: 62.7 MB (62679539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839058186cc83bed69943d6a02ef5edf123523a4400aab23fdf16a0bedb770a9`  
		Last Modified: Mon, 21 Oct 2024 18:57:17 GMT  
		Size: 109.1 MB (109102260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7ae21098b60d1fe5a51292ed061ef2200bcd0f9df4b4e7710cad511f25f4cfc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5885744dd2bad850695e6a75736c3d2735b31ffd1224978ca32e60b5c6c26e`

```dockerfile
```

-	Layers:
	-	`sha256:8ce483ed3843b3b89520bcb2d71aac030f69d6fb18ae296858c514e417b23c72`  
		Last Modified: Mon, 21 Oct 2024 18:57:15 GMT  
		Size: 7.5 MB (7497744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5b5bea838b3858724961cb0560426f5d67ebd4933585c57037e6b2a5bf75ca6`  
		Last Modified: Mon, 21 Oct 2024 18:57:14 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:02159c9aea6e6e954de8dc082d93d76113506c1a8405f1c0125cc7bec56e4439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117526572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d15cb09431a69c9e80d565f99b308a9d22f2dde487ec87c4d53bae39dc8ba00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:c05d42ff0b796ff4b1055b91676cb7e4b68389f23472cfdf987fa036f88561a9`  
		Last Modified: Thu, 17 Oct 2024 14:51:33 GMT  
		Size: 64.6 MB (64587089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a906f427c34ed817cff73def0c3761d04e4095eda0b67e50e87df38a58a692`  
		Last Modified: Mon, 21 Oct 2024 19:14:55 GMT  
		Size: 52.9 MB (52939483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ccc1451315d8b74b3dec031d1f73a0a873818c55b789576b0fafc35d460bb99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c251c2b92ca9f6043158d4ef942da91d12079b1afaa1726d335d1dfb8a91bc18`

```dockerfile
```

-	Layers:
	-	`sha256:b26b94da3df3cf6008c32b045741e2d35a0537584c42a00fa68b2683981ee66c`  
		Last Modified: Mon, 21 Oct 2024 19:14:54 GMT  
		Size: 5.6 MB (5613464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:758a368d0af1c8ef71dac23733652cacdb9a65dd213cfb0caf50f178443eca64`  
		Last Modified: Mon, 21 Oct 2024 19:14:53 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
