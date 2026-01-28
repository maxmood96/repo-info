## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:c25fc9502032f318c8c90193972949cf89095f32da723756c04c4ef533833ba1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:93284efd249fdf2ac7785834fed25c5c15c8835985d3c135255faf0ee54847fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228722811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022d2a0ed89e30f0fc008daf141b1fd9be375dd315ce477c6bee919a5b493bd2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:45 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:13:37 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:13:37 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 27 Jan 2026 22:13:37 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:13:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edaf4addd1dd3d250a4e9cb383f63ca643d4087457e6bbcca67f3952582dfe32`  
		Last Modified: Tue, 27 Jan 2026 22:14:00 GMT  
		Size: 165.8 MB (165759102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:42b5f490f25bdfeca1510da3556ed5cadd6491d90a5c11f667707c216c1f6f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fce5fcaa761dca35203d06ae626c6cfd0996ca892ea6b159d24320757829e6a`

```dockerfile
```

-	Layers:
	-	`sha256:4f4ffde0c83254e7543d4fe309d446c2593f616dcebefbeadd90bbc8c2a36ec2`  
		Last Modified: Tue, 27 Jan 2026 22:13:57 GMT  
		Size: 6.0 MB (5971814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:756c2ff4ff72e170a7c0236ae506cbdad5ce1a478e872283e4d70c5071729154`  
		Last Modified: Tue, 27 Jan 2026 22:13:56 GMT  
		Size: 9.9 KB (9914 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d1066ee9b752907fcc42f3dc04774535e064c444aae5754d7a96ed8a95b22462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221079050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75fe66809681219130a3d45991ac2f36524d474f94e8c5d384b94dd03e5b3989`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:34 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:12:34 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 27 Jan 2026 22:12:34 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21991912868cc859bdd7379836d8c0daa2354285345c24526f85277f2e659cca`  
		Last Modified: Tue, 27 Jan 2026 22:12:56 GMT  
		Size: 156.3 MB (156280161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:842f4fe9ccf37897ba116a6f162d39b8f392baac00a827dcf0615155da8ab613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e02fec32ffab73aebc9395fa2dc4f7a091ce90811b3aaa2e49081ec406ac6b`

```dockerfile
```

-	Layers:
	-	`sha256:930b915b9241d54c576f63b88d7e78b8b440eb04d23976765b5c6ca910342381`  
		Last Modified: Tue, 27 Jan 2026 22:12:53 GMT  
		Size: 5.8 MB (5763684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd655f5fb74ee2ca15a7475e07096e63e52199e7a2b10f61ca230af9ca8611c`  
		Last Modified: Tue, 27 Jan 2026 22:12:52 GMT  
		Size: 10.0 KB (9994 bytes)  
		MIME: application/vnd.in-toto+json
