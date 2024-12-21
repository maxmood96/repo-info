## `amazoncorretto:8u432-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:8e9441b455cd0169149b2cf74cfd2846cca44d5163eeee19687c1f43338c7e9a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:372a236b591dac4cffedcc8e4513278134b71ee72fa0d4e6603ded4f6b3bb65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179925202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1eca565f926a5923319650f71cb5d4d037f59fb0d3a32208d797dda4038c06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4119095d54bffc42f26c4551eb2a0241897ab588c9f058f7be12797bd7207a16`  
		Last Modified: Fri, 20 Dec 2024 22:30:59 GMT  
		Size: 117.2 MB (117247763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c8affcb75ce4c76b2bdd95b0aaec8850f31952108b4984e466ca3197ba2f141b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39dc0c176c2a255c3f40d3164c0eaaeb7e4ac2b3de8d39ed23065d753c0aac4`

```dockerfile
```

-	Layers:
	-	`sha256:e6b879bac16058498991fe05a6d97ef54571a1131a813320397cdc34524eea6e`  
		Last Modified: Fri, 20 Dec 2024 22:30:57 GMT  
		Size: 7.5 MB (7483483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79792013d431d0ab213e1531c091a3660f0c544f21bd57ac9efe3849e4b07b3f`  
		Last Modified: Fri, 20 Dec 2024 22:30:57 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8cf8fec3e38afc6c274816325e9a87340b573126fb2197a3065be16e5efe9fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117511430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95be305a46ddb29b8f3688ab5a424e591639e2adafcb27b961c007c77f48a3b2`
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
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d7fa6382a4fc2f83ad27563be8dff2a612677570d3aca022a8c4e5130530f0`  
		Last Modified: Sat, 16 Nov 2024 00:50:00 GMT  
		Size: 52.9 MB (52929543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ea7bf5fdc7784468557b440f1e163100d6327b6068cf27a903e30fc28a98bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89609bd1813a04d06e8dec990f5287fcaaa1c4599b8d0252b8c859a1a389496c`

```dockerfile
```

-	Layers:
	-	`sha256:91e450463aecd30437b5cc52a35be196831ee35b5bb3c67456b1d9af07f6777c`  
		Last Modified: Sat, 16 Nov 2024 00:49:59 GMT  
		Size: 5.6 MB (5613464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c3594217cfb3d6c12f671af55b6173b1a3683178e1edebb3f245287f0b37d7b`  
		Last Modified: Sat, 16 Nov 2024 00:49:58 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
