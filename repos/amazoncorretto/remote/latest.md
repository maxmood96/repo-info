## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:f12dafd3afd1ffbad3a44daa67b9d5378bdb9371d022e24cf1faee7cf77a566c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a6bae05c74c805954466fff36a958b56920287f497bcae95c2f6e30a115fa682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138196912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6cdea880e5e95883f5b5ae37a2bb2a0396da449a794e75449cb71d35cfd0d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:15f372c0d55f5152b222fa508a1a8c382d0621d72fdef0d2b746557a14bc0dd9 in / 
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
	-	`sha256:1e5e0347739e5468c65eed56d50fba90128674d8aae6fa196a8c01eeea145da9`  
		Last Modified: Thu, 18 Jul 2024 21:20:18 GMT  
		Size: 62.6 MB (62647926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd63355deccac1714e00a85da12dc04294df01afee7aec11ed51bfc2106b84`  
		Last Modified: Thu, 18 Jul 2024 21:49:10 GMT  
		Size: 75.5 MB (75548986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:52bda9d1fb6348cb1fdb23f1748fa2cf7177cafb06a23251564bd08fe53d9c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57c0b545c42c962aa9a0deb69b492a4290f4ae85a77e43afa63bfb431ca5ac2`

```dockerfile
```

-	Layers:
	-	`sha256:094eb502fcad1de97e4f464d351a037ad8df691634ae0444db23f7a2fa28185e`  
		Last Modified: Thu, 18 Jul 2024 21:49:09 GMT  
		Size: 5.4 MB (5369674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b934aca17b6652e36918108f90caeec935c5b6fba1714940834f46506e240be`  
		Last Modified: Thu, 18 Jul 2024 21:49:09 GMT  
		Size: 11.3 KB (11331 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:latest` - linux; arm64 variant v8

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

### `amazoncorretto:latest` - unknown; unknown

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
