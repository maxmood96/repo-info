## `amazoncorretto:8u432-alpine`

```console
$ docker pull amazoncorretto@sha256:121f0c3170b7f2cedadb6c2eb9e006c7c31d75a60eafbeb17e276948352f9318
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5aa8f6c713446ac0cc730c80419d5bd9ed5cde3e3574f152b00c341dd93e0484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103809160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a571726e1fe4fff10fee79d5e0a19cf3667688394377644632bc99d97e9131d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f23e43e6f53084bf3510b05ccef4cd071b41ae953296289e0049a62aa3ce93b`  
		Last Modified: Tue, 07 Jan 2025 03:28:46 GMT  
		Size: 100.2 MB (100195161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f323b22ce2a025fb2a46a8e35769c6bf8ed631209f75c9bafdf42ed5ec6bfe3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 KB (253396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2a78c0c9504d39c6b185a52b34fb1b9ab40531d30ad44cb6a8ee0b764968ea`

```dockerfile
```

-	Layers:
	-	`sha256:9bfb0b95e760912c02cf4c29d02a3c13de4005f1c99794e37b0d9a04101efa4a`  
		Last Modified: Tue, 07 Jan 2025 03:28:44 GMT  
		Size: 242.7 KB (242700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7754ad77202538fe0032d6514b565a0ac39e9d27ff884dbb6acd1d65a0b4463`  
		Last Modified: Tue, 07 Jan 2025 03:28:43 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:95d92c1ccabeb6e02e6271c9f3c0bf65eef270dd68f5477f9c12302ee6b13e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104066538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc3bca5f49a6d7936d5c7599c33a0c52f467b59b4187267edd13d3828e5d9e8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b0e098319e117f1f4d0badd0956f33a6df1ba40a57556a74b5b6d5951a713d`  
		Last Modified: Tue, 12 Nov 2024 11:05:28 GMT  
		Size: 100.0 MB (99978812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0db7e1a696754f1fcea40b74971d561e817a250eb515305d74858dbe2fad743a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 KB (253974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a7879ce1616e63f9692ea4f7a576c0362dc2b4ee7fef8ce10721895ae6393e`

```dockerfile
```

-	Layers:
	-	`sha256:416c04686662ebcba05a121b2d3feb1f6d925a18eec81a06845af2aefe5ae01e`  
		Last Modified: Tue, 12 Nov 2024 11:05:26 GMT  
		Size: 243.1 KB (243128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57ffe1863fa5d44b37c3843ec7f3a3d2546c65b257665fd1f4ed06aec7afbcd9`  
		Last Modified: Tue, 12 Nov 2024 11:05:26 GMT  
		Size: 10.8 KB (10846 bytes)  
		MIME: application/vnd.in-toto+json
