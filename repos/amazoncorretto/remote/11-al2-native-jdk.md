## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:447d89fa74f8ca0fc229bcafa46168cba4458532635564f362f613bb7a2fb291
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bc0750ea6ec395e627cc1533ad8c7595aa5ff64598a010dc0dc9ffbf2bc6bbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.6 MB (224587276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f680bfced43b91a66c0b5c404921196e1e8d1b43b2bdadde9960106b9bfe20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:33 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:31:33 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:31:33 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f149064213e817f38af03ba821d5bda94e074bed4c2e5da0de102f6eb53375`  
		Last Modified: Tue, 10 Feb 2026 18:31:56 GMT  
		Size: 161.6 MB (161628319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:089f44d6654053d3a1893b1b7f7be389dca6b6c6a83a004e92e22d32793d4ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (6004479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887c8db46e0ab1649a85364dcfb267fce164945a048719be4f19dbc755531c97`

```dockerfile
```

-	Layers:
	-	`sha256:44a1ffd98f3ee7a10be808fbf79c2cc8eaa71d902b220d8fa836715db571ed03`  
		Last Modified: Tue, 10 Feb 2026 18:31:52 GMT  
		Size: 6.0 MB (5995082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5665862e3f873c8a7509f4ab3bb3116c48b50a3e4142b5d3ee20ba8575c59430`  
		Last Modified: Tue, 10 Feb 2026 18:31:52 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d0a9cc5c82623a66d4eee7d7ec4f720160b0209adae1ee2fbc05453b6e7fb362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216529313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2a829e38be43bbb8c7db2928d23e53c78cd6659c744cfc9993faa116d95769`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:26 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:31:26 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:31:26 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd523acc1f70a30c54134ef43272cbe31a0bfe9b13278c29e48b95af13d03e0`  
		Last Modified: Tue, 10 Feb 2026 18:31:47 GMT  
		Size: 151.7 MB (151729837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9540468db5327b66ec55f272a58014a2122017b32e4f13043d2b037b0363bb95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5797272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d03b8f7900830bf90091f42ec79cfc958129818cd5813d658e8ceed88a23ae`

```dockerfile
```

-	Layers:
	-	`sha256:98d246ff8fc238acdac38e79042952aa57d314810cc7e7bc924b5771b557ca33`  
		Last Modified: Tue, 10 Feb 2026 18:31:44 GMT  
		Size: 5.8 MB (5787796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef8baf63fbd827828093d1b2ffabba6909043b28599f8f96529d720facd3ab4`  
		Last Modified: Tue, 10 Feb 2026 18:31:44 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
