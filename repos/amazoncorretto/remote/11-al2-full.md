## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:b405f23ba088252d6c15aabdf71cbac5a8c0b527bfa8e96b4122c5b78eff8cec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0c2348acf85d3b1ab4bb13ccf936f12e27c312a9d79bafba9b34c88b81137fd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210781968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70df672968c940a68f575faa871328a9661bd915898c921b651dcd2d52b9cf90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:19:55 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Fri, 28 Jun 2024 00:19:56 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bff70b9d0b7e74dcc8b80ae7e25e8b8aae11d031bc905de97aa3df1360d11e`  
		Last Modified: Thu, 18 Jul 2024 00:55:53 GMT  
		Size: 148.1 MB (148135330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7feb91c5be93064d3fa4755ba6bfb78c6045c5968de5d3aca3cddd41dde5407d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60432e43d638a69a4fb8d4ce4ea8ecf18ff6c09b4a36516696f690b2b9582de3`

```dockerfile
```

-	Layers:
	-	`sha256:40e3eed114805552dd45a891af7d0e42dd6ded7298927dec7786698b88c07457`  
		Last Modified: Thu, 18 Jul 2024 00:55:52 GMT  
		Size: 5.5 MB (5535073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d10cdbb73022b83c50fc101dbe4c865bfd1df348e322cf54771acf4cd6807364`  
		Last Modified: Thu, 18 Jul 2024 00:55:51 GMT  
		Size: 11.0 KB (11016 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bb06ab1e9f1c32bfcc1d2a7a106fbe47f45cf5bba0d85015ca224f71f3dfada7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209819595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e678be5fddcf2803efb4fa3701bd2071236d2207ba6d4f02d07b5fd85c9142ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:40:02 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Fri, 28 Jun 2024 00:40:03 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e131ce93a081d7caa0051a9bf60e0312c77b18d06b15d5637200e0a9b6ab4240`  
		Last Modified: Thu, 18 Jul 2024 01:02:46 GMT  
		Size: 145.3 MB (145250830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a6f7b06ba56d42ab9268d0852d65cde0dfa756ac2110981e9d001b5a0ad816d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c9318f3833dd5f0d4a5ee0e4035c3be4ce6e8a20da66d6e2270b94bd8057ff`

```dockerfile
```

-	Layers:
	-	`sha256:cb5201e2e8ae470fbbf7d1a085f5a420ecfd13cf906bb8c16718f41d24e058f7`  
		Last Modified: Thu, 18 Jul 2024 01:02:43 GMT  
		Size: 5.5 MB (5534566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd2509c374b381087255b966f8fb4d3b0c87bdddc6a734f448d1e04730695259`  
		Last Modified: Thu, 18 Jul 2024 01:02:42 GMT  
		Size: 11.4 KB (11366 bytes)  
		MIME: application/vnd.in-toto+json
