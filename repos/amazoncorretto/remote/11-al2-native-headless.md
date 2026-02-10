## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:73250af50d7ad7beff3c1fbb4f0c63036c3cc2d9e5b02c094cb9cbfdf78acb80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ff3cc280bb07eddd51c4bcc4d3e2a0cea1bd566ad32bd4046c89f2175431cbb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217288662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a969c677fdfc149b79b1646bf02579a4ee8e0d51e5ed48d4f1b8ccccfab596e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:08 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:31:08 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:31:08 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1fcd26c4edc02f453e634cc5ff5a2db9457ef128f3543d19427e6d470247b`  
		Last Modified: Tue, 10 Feb 2026 18:31:30 GMT  
		Size: 154.3 MB (154329705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:68a3bb9e62bad204b1b0c9b673915a4f5ab16026cfbc5f59cf88345957c8047a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7278563938fab684e09af6ff04de9907ba197aa3540a13947bfef03a7880190`

```dockerfile
```

-	Layers:
	-	`sha256:02970706d8add519ceef944377435f4c375da3579d6eec92e8019fd4481ae33c`  
		Last Modified: Tue, 10 Feb 2026 18:31:26 GMT  
		Size: 5.7 MB (5683305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b488adeb5ecf0e14bdb587afc2063bf7a0cfa052ec8cea91d3844de9426b1608`  
		Last Modified: Tue, 10 Feb 2026 18:31:26 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a16bea4675ced65ebdabe199218b506cc3f0289145bbf85a3117a579222c4600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.4 MB (211421981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb64c6540c8adc9ef968806d13a48acb7406e596ab3108467b17d61b62f10dd6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:24 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:31:24 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:31:24 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868876175c2968c5dd2dadc6a4247d52a52606af715e4c866dcbad78b69974ef`  
		Last Modified: Tue, 10 Feb 2026 18:31:44 GMT  
		Size: 146.6 MB (146622505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:00591e30c362b5cb036ecccaa9e0e318a00813dad53bb51828558fa69c340cff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8966d14d1b2fe3ed17fefa79e260309fabd9b2236ff7b60c10b5d7f5b8feffd`

```dockerfile
```

-	Layers:
	-	`sha256:0d5ceb3f4371da2648cb8be9e433528d966f983c3b296b0eb0cefd68625648b3`  
		Last Modified: Tue, 10 Feb 2026 18:31:41 GMT  
		Size: 5.5 MB (5501773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7a4acf21c5d281ea29aa17d298f7a31d12e59fb45a19956ea622e630025ee25`  
		Last Modified: Tue, 10 Feb 2026 18:31:41 GMT  
		Size: 9.4 KB (9367 bytes)  
		MIME: application/vnd.in-toto+json
