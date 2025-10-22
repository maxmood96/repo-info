## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:0c5b6bef7d4fb844e45648d5617406c8e7ae90929aeaef74fc621601ff3fda15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:30276fd00e7c6a991ca22fd4f7edf0bceec1036bc1941395b17a9c4d728bee2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228428558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8f70fbacfd04d147819ca2fda7e17d0e7f7ea0e5df494f5554f45884a4808f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d592fe075709c62638ad9b0b8b67157100093faaa06408e582bdceb37cb6083`  
		Last Modified: Wed, 22 Oct 2025 00:36:57 GMT  
		Size: 165.5 MB (165487938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:707c1efe302ee5646b0e9cfc23e08111dd6f141f7a6e9196976a39bb808b02d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfc0cdc95e5443aa2820501a753a5f14689188c50469bf77b06cb881b750b1b`

```dockerfile
```

-	Layers:
	-	`sha256:86a42fe8e9a9f439c069d6f41b6c7913484f3105fef45d29038d75f0a8f47ca2`  
		Last Modified: Wed, 22 Oct 2025 00:51:30 GMT  
		Size: 5.5 MB (5535595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e566757abc9f06d33f55f4e6d968e5b4102f71cf1c30b24ce43c8d71108147d7`  
		Last Modified: Wed, 22 Oct 2025 00:51:30 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7f5d7273cb2808d5e0a2bd1a920c088ffcd3ce770e499e85bfeed3ba645a8573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228380396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc0733103a8a4ce49746bb31fc2df2691c650b43566bbb061add0e19e31154d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:41 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007c99654ecaa79d9c18ade13301c62620d4fd6ffa16a1f4b1d2b9003f55592d`  
		Last Modified: Tue, 21 Oct 2025 22:13:26 GMT  
		Size: 163.6 MB (163587188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:173cf91c4f626ebfd93b221aaa6554c8063931affafa46fa3aad741a2ee24847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47a37d5c50a909feb0fc27ac6195d5b930578fb15a668953a7d7d32ee0d67e8`

```dockerfile
```

-	Layers:
	-	`sha256:c1f26cab52d9e07a54d8fbf3c6c2415b9cde308a896dbfeebff041ef6dd84c41`  
		Last Modified: Wed, 22 Oct 2025 00:51:34 GMT  
		Size: 5.5 MB (5534284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:659e6be087542396ee4649a01725ec405f8dfa5c8d179442c5b7746fb7035cb0`  
		Last Modified: Wed, 22 Oct 2025 00:51:35 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.in-toto+json
