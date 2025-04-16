## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:23d9d6546dcbfcf1e828fea2b66be53ed11d6a9e676837fdf037123a80ed84b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d373a186ef88cb4d4a8abd0cf8b06f0938ffc336bc02354335d6b0844961fb2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214503532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9695d38d562126fe80e4e398ec55d017450cbf421221abc404bf20d537bbc1f9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:37 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3b5771a528b1220f7f687181fc0cec216aed88a7fd109a223e795a33dcb1dd`  
		Last Modified: Tue, 15 Apr 2025 23:55:59 GMT  
		Size: 151.8 MB (151750643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dd05b7c11715eb347f8739ce35e289d4cc297e81480d7042285bea26122fe176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f52fe08a420f4299735ec280a16ed2c42c5edf2c115e5b19a70cbdc8072b7ca`

```dockerfile
```

-	Layers:
	-	`sha256:e291ebd6943e51ea09e4528b6abde45de54c134a7e34c3ad85f471b9b4e2496e`  
		Last Modified: Tue, 15 Apr 2025 23:55:56 GMT  
		Size: 5.5 MB (5517134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a120124ab1053355f84f4aeafd99d1dd3c1568173a1dc9081dc3ad619f3b6b83`  
		Last Modified: Tue, 15 Apr 2025 23:55:56 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0011a234aad2575fc434b7ed17cb99c2679d4ba1a1a06cbee0864af2092a579f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214949932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4bf1d871cec0dee738ce9d4234a4b2f71d9491248cb5f1104bb3e38db49631`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc78a794204205caf229722289ea3beec64dfead5533793f7446dc927d5a3ea`  
		Last Modified: Wed, 16 Apr 2025 00:08:14 GMT  
		Size: 150.4 MB (150384110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:24f5b1056593318d4b784841e324591c5780575490c5188decebeabb9010b01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85040540e5eb07f8c2b32808e1b6623fb6cdfb4225df1e3b4a5f0b656e279add`

```dockerfile
```

-	Layers:
	-	`sha256:52b3abb417c86f005161d1e89308e8d4e2c3b944af1e7faae58bba6f2d1102d3`  
		Last Modified: Wed, 16 Apr 2025 00:08:10 GMT  
		Size: 5.5 MB (5515823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859cca0c9ebe4f7f3360332e6415105e97465bb1d20de216936b695edee189a6`  
		Last Modified: Wed, 16 Apr 2025 00:08:10 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
