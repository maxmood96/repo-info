## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:885410aadaf4921aa9abbe7676a07d087508b9cb64af780618d1681c169a110e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a07945708e8892559fd4b2d799519fa36c8dad913b68444684d4ad91eeae1049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150541858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40cdd70a13f6adfbf5c00e173e2c266153fda64e235ec56801f5387b0fc8aec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:dcefe03e9009da4739e237894f3fe49af6782d53d9e2202e46127bd568617855`  
		Last Modified: Sat, 09 Aug 2025 04:15:21 GMT  
		Size: 63.0 MB (62959372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7471d2aeba0e741dd0922bb9bb09de7075e55a4f22cd3691a7d7fecd0b900d1d`  
		Last Modified: Wed, 13 Aug 2025 23:02:50 GMT  
		Size: 87.6 MB (87582486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9a77f48a9fa4e45e4b048479ff02907e34ed0cd861db8adf8910cf46f3a8adb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dea382673598eb128d229096f92c2dd06c62e39420073e87e9bfcf6f04bbcaa`

```dockerfile
```

-	Layers:
	-	`sha256:b4d670493565381a0b36c2bf1f1f1fea7b267d99f109cb020fd0dc754ade733c`  
		Last Modified: Thu, 14 Aug 2025 00:48:14 GMT  
		Size: 5.6 MB (5631755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a7b7e6dc5196206119a0bc5566e9bb0ecb334534a5eadd5f66cb8dbf4859384`  
		Last Modified: Thu, 14 Aug 2025 00:48:15 GMT  
		Size: 9.3 KB (9336 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a467cd07d140d5f77375a93535c033199102e7a13e2387b086ec8e5e3371ea9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144582924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2d250f99bac7c3f6145377fa24e0f94e27a95be4306d2a4a5a0fa8535ac2a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=17.0.16.8-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=17.0.16.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d111d038f27b707b8e25fe3ad6fd956496b43d5096687fd370ded249420f2b93`  
		Last Modified: Thu, 14 Aug 2025 13:52:31 GMT  
		Size: 79.8 MB (79788560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:be82d3e32e12c2269e1f694f72f00182004cb9c1522e6ff761bed9617bee0361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a9779bf8c4c631b775232eabfe18ad08f041e3084caeeefb6c5b2460d50d7a`

```dockerfile
```

-	Layers:
	-	`sha256:e195f7a27a7d1dbcacc2f6ed76ea7520e5e4abd737678d9d4fe8dbcec3ae77e3`  
		Last Modified: Thu, 14 Aug 2025 09:48:14 GMT  
		Size: 5.4 MB (5448031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c73d907a485466b15052974e461d7f2d6e2e386600cefb6ed8a6f5f5c8d08d`  
		Last Modified: Thu, 14 Aug 2025 09:48:15 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json
