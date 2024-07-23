## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:2d44d96772e738cdbe9d7cdccee1752d57ecb5e93fd36559d827bb6bcbc7affe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c96891728a6c1472a8090f4d41b5d4fa239601e336775ebc97e866e41394c787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138198312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f71dd463e53bcfd9509b0fef2dcbf3d3ae915e7178fcb67c8906e62b26ceab08`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:23:24 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Jul 2024 21:23:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:37766f9d8ddf179208313163dc89d8d39dc16ba3be3bc46534855c244565cdd4`  
		Last Modified: Fri, 12 Jul 2024 13:12:20 GMT  
		Size: 62.6 MB (62649406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddef3542383b6cd2355a022d5cbc1c3e55afcd0e9579fb0f8c8c3ab9e82f902`  
		Last Modified: Tue, 23 Jul 2024 00:07:21 GMT  
		Size: 75.5 MB (75548906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5ad49f15543d1096014ce622213385e80d36aec23fc35fdb648972a6b981e26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b6eaf19bb6a9fc7184ae1007699550a0a5c7ab64829ddf8ff733afa8a3e3ee`

```dockerfile
```

-	Layers:
	-	`sha256:6aff93f8aa56580434dbb08c30175e741ce7dcab5da22d65fed7080df824ab92`  
		Last Modified: Tue, 23 Jul 2024 00:07:20 GMT  
		Size: 5.4 MB (5369674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b603cc31b7fa08013ea5f51fa01966b716602385fc39bfe44222874ccd00ec92`  
		Last Modified: Tue, 23 Jul 2024 00:07:20 GMT  
		Size: 11.5 KB (11536 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7a64e86411c855908849032426b0515f24124fc2eaf22bcdee3888ba92df8845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124239232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3a58e76e2945cf5f9a0256e1b7ee09e01595a3fd0b31f3cc7099a54cf53607`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eb1b24b2c82db919ec9d4ae81fbf5fc35b9434d43b0734066aa19da336490f`  
		Last Modified: Thu, 18 Jul 2024 22:49:44 GMT  
		Size: 59.7 MB (59663921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:034a5a06a46db8ff870c113713824fab72bd1e97f116aa3ed9dc61712152c195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5359914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f256b222da1de6792140c61936957611f12b977f51a468b46ae0997ff73b035a`

```dockerfile
```

-	Layers:
	-	`sha256:6e5aba3496903bb78893e0f1ffd39e85f9a8834b412ba83f0fc0885d6fb9ec67`  
		Last Modified: Thu, 18 Jul 2024 22:49:42 GMT  
		Size: 5.3 MB (5348221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35f0254b3dd17d6e40909f8bfad2ccbffaa149b9ba935697084b88044c811ff0`  
		Last Modified: Thu, 18 Jul 2024 22:49:42 GMT  
		Size: 11.7 KB (11693 bytes)  
		MIME: application/vnd.in-toto+json
