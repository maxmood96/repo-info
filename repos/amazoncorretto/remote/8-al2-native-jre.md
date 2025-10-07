## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:1b9d94db8f078e22ef46b4908bc63fe81082a3f1b221c7917c47c076debd42a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:24c800e49a9d24892fe3a7b05e7111db4456c025bac093bb105f5692f4a71aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172050575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac7172d0c80d8c285514b8314e1192d118aea86be6e00001c2ca4c55d9b74a2e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=1.8.0_462.b08-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618a4030c6d9eb36da84740fb3183487c363afbc9bdf2f6143d904cb57cd5e82`  
		Last Modified: Mon, 06 Oct 2025 21:10:15 GMT  
		Size: 109.1 MB (109109955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0f51cfd7fc5a56f56e50a6665ff2052e14934fe07c6f9ffb94675194b8c28e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851d91996572db3b16c7babc3cdb3371713b0cb97d72b2d52aa98896ab071410`

```dockerfile
```

-	Layers:
	-	`sha256:6d92dd86b67454954eb4b697087bb3e562626ea858de45a741521e1106b39d4a`  
		Last Modified: Tue, 07 Oct 2025 00:52:39 GMT  
		Size: 7.5 MB (7504128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ef3659358db10b89cfef820c5dfeb0997bcb24a5f2de7e85be5c2ccaa6bd14b`  
		Last Modified: Tue, 07 Oct 2025 00:52:40 GMT  
		Size: 9.5 KB (9547 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:902d55c9f25dd400d4cc7b566d7cb2b1785c46a026b41728135e67cd90274c25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117727843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a95125382ae246e39dbbe5f0dbe59459cb904f2ab39f804e4ed4214dce3f9cf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=1.8.0_462.b08-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2c00db9fc61336070406fb452e42ee058340a2da62d7af8d96174df82667a0`  
		Last Modified: Tue, 07 Oct 2025 06:06:22 GMT  
		Size: 52.9 MB (52934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:68b974d5f5387b39aeadbd91d2e973798beea0e56dba2ce33a512d1cc389a3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5080c6acd76d6f724b3476b6c5659cb84e041368bafb2ee519709d7fcc21f07e`

```dockerfile
```

-	Layers:
	-	`sha256:2ef4538b25bbdcef6e9ebc4d48683414fa30e5a60b5e2ae1132144a4b1d3cc1f`  
		Last Modified: Tue, 07 Oct 2025 00:52:46 GMT  
		Size: 5.6 MB (5618887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d498af8be81464e55b8685392991420a2d479fdfe34ce7442a89c381705df02b`  
		Last Modified: Tue, 07 Oct 2025 00:52:47 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
