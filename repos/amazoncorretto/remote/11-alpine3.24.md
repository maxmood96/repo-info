## `amazoncorretto:11-alpine3.24`

```console
$ docker pull amazoncorretto@sha256:e59672f2c2a7b473802626a7d0fc45de3fe8248dcbf30a38a507c5ca1a0033fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.24` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3366ba185f54ff58f0763b7ebbe597fa0e9519d8c72b97fe4c8af06dd8435e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147558498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31d5099e56927fbc2f7f9a4ce19aa7916e41a41eb6b0850498cae7e8bc4f45af`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:20 GMT
ARG version=11.0.31.11.1
# Tue, 16 Jun 2026 00:19:20 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:19:20 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:19:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:19:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd05ab84418d679b0cbd17930ab8ae0f501d530d01b3010e9127bef7ff2d9d4`  
		Last Modified: Tue, 16 Jun 2026 00:19:38 GMT  
		Size: 143.7 MB (143712107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.24` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:45b3e183007c78e3abe8341a4d785f725603a83bf75c9257fee7196ce25863a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.7 KB (599717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9f13ef38f6934f654a68a92d0564201895ed3ff844ddff41682e648ed740f3`

```dockerfile
```

-	Layers:
	-	`sha256:84a13250efd7a2999ef4d844bb4047011e1736d01356169eec478fc7ae4bcccc`  
		Last Modified: Tue, 16 Jun 2026 00:19:33 GMT  
		Size: 589.0 KB (589030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f44f90e9e8fe056682ac35bb5b6776e89f6a66545774c6944b0a41710b9fc8bd`  
		Last Modified: Tue, 16 Jun 2026 00:19:33 GMT  
		Size: 10.7 KB (10687 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.24` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:059189a3ed16ea944f2fd1a24bc25c75327e6b417e586647f165a323947c5e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146160869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6f902d444f3de366bd8151d9a045abbec6271d74a2a4ffab11dbf47ecdf255`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:31 GMT
ARG version=11.0.31.11.1
# Tue, 16 Jun 2026 00:17:31 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:17:31 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:17:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:17:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2379e7ac2d3112fce3f64d9467e0e7bc41de0426fcb06d70f72ebe1b22dfcb`  
		Last Modified: Tue, 16 Jun 2026 00:17:48 GMT  
		Size: 142.0 MB (141977832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.24` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d627b8a5fad9a55f6ccbecce88d32d79eaccb1238d8dca24ecf4974666ce8f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.3 KB (599323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1738ceb5dc831225798b382710942ba70beec826a692d255e24ec0e4898fb34`

```dockerfile
```

-	Layers:
	-	`sha256:4e2ffb4a713bc300aa485a3ec8604d44b02a3b2cff4083be3e3ce457ce477341`  
		Last Modified: Tue, 16 Jun 2026 00:17:44 GMT  
		Size: 588.5 KB (588484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ab3266be62b1ba9b5ece34c9a127c8afa5f8b55fcb8293c8511f4a66e5f5b18`  
		Last Modified: Tue, 16 Jun 2026 00:17:44 GMT  
		Size: 10.8 KB (10839 bytes)  
		MIME: application/vnd.in-toto+json
