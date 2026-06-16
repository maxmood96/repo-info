## `amazoncorretto:8-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:aca49af8d03b05cfdc688d19df56b5416edf35b885b24ccba6640257fcdc2d47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c4f692061a1d02bea59802552f81863887335300bc37f7adf35c1de5bd9ae087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45596451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:194878509700bb2dab2eb6b01d6794cca3144875081b79980054e4704985bf57`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:13 GMT
ARG version=8.492.09.2
# Tue, 16 Jun 2026 00:19:13 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:19:13 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:19:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5d800c13cb6bb42f93e0051a2b4ca80714a155bce8736080e0495edb9cb13f`  
		Last Modified: Tue, 16 Jun 2026 00:19:22 GMT  
		Size: 41.8 MB (41750060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:621d96b17e6860f38594712633132aaa03827a4518eec6f29e910756274ce9bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 KB (197254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0eb209a3f6325530571462b8757e8e16ac35a5402875449a4ca4e9c6d7babf8`

```dockerfile
```

-	Layers:
	-	`sha256:2e418a71542bae74c5a150cbb44c977599fba15a6e6c187ac82e7342792fc750`  
		Last Modified: Tue, 16 Jun 2026 00:19:21 GMT  
		Size: 187.9 KB (187938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1766d976dcb1e810962f5a074d5fbf87f84fc31f626a53c22039b675c6df43ed`  
		Last Modified: Tue, 16 Jun 2026 00:19:21 GMT  
		Size: 9.3 KB (9316 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ef663a94c52ecc8b40ad4937a66dd3ed9fd58d44d5c7d66d90c9de01b14b8ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45650821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8c614efaed6b292a1e37a7fcbe7ae6dae6b2befb629bca56b8d2e7b8be7536`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:24 GMT
ARG version=8.492.09.2
# Tue, 16 Jun 2026 00:17:24 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:17:24 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:17:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ca60a56c5ca143d9bf5a3ef540c98cc877238b46dfdbfd66620bab2f163157`  
		Last Modified: Tue, 16 Jun 2026 00:17:34 GMT  
		Size: 41.5 MB (41467784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a9be44168f1368f67eea144512cde8f50afa99d7afd54af28f5b7b356d9c47ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 KB (196840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb084a841328184adb37ca6f0c8bf0e5c2afeea406f0e253d0a84624ffb7804`

```dockerfile
```

-	Layers:
	-	`sha256:940e2470584045eca2c16c36deef8189c8a4a9dc00ef20ec5701d702f10290db`  
		Last Modified: Tue, 16 Jun 2026 00:17:33 GMT  
		Size: 187.4 KB (187420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a079391380de6810377b7b98dc281da803d7ec27594aacb6359dd2cab17957e`  
		Last Modified: Tue, 16 Jun 2026 00:17:33 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.in-toto+json
