## `amazoncorretto:8-al2-generic`

```console
$ docker pull amazoncorretto@sha256:26276ab73e2e503c4e3f33778e3b2e7a6af9df6d6372160f23af27454229b243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dfade8be818792ea5d6a839437ce46534952790d29b86f7c963fff2454bb9431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138186453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea5de76f714c0f1c48cfe1cf40e883ebb75d51d01565f8036d9512db6ef6fe7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=1.8.0_412.b08-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed49dd100acfe5974f64f71d47c63e45352073ed0cb7a6c0cff1a0efd58a8e18`  
		Last Modified: Fri, 05 Jul 2024 19:56:14 GMT  
		Size: 75.5 MB (75539815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:83825795df57c961887448be304cd3aea2d20fc04e26ea5445c1b13c619a31da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb625454faab62cde5e298877349b8c64667167fb6a51d48f7b863311246750`

```dockerfile
```

-	Layers:
	-	`sha256:e2d5633b9d7f6de3d43666da09f478bb2bb6963b3762f6059d06caa0d58e03fe`  
		Last Modified: Fri, 05 Jul 2024 19:56:14 GMT  
		Size: 5.3 MB (5344707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9188b1951aff3fd27a1a0754b91dc304dffa4e6e6f3d5805a2afb02aae001cb9`  
		Last Modified: Fri, 05 Jul 2024 19:56:13 GMT  
		Size: 11.3 KB (11330 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9c87d5af64bdb603484dfadfd127f4d4e10c29be566c10a193dfc8b64c2ea208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124219014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db60529ce23f97b01273021de74ef843ca46bfc960324e7b639460f0d03cc89a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=1.8.0_412.b08-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cada1bd9b04a15210b907122920931347f196d760f887d499c8ee0bec8c67b10`  
		Last Modified: Fri, 05 Jul 2024 19:56:18 GMT  
		Size: 59.7 MB (59650249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:83542feb187623ef05d0ee7da91313acadd2a4fd7f3b896c70ca4faa30d17438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:074192430d21d0cbb487faf3c4cce827c88d2d9f10dbe20e14e3805469518787`

```dockerfile
```

-	Layers:
	-	`sha256:9e4357b39a9c43c5dca9cf39d2fd7d8067899dc5e11a9d3db8eeebe40603be61`  
		Last Modified: Fri, 05 Jul 2024 19:56:16 GMT  
		Size: 5.3 MB (5323969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4263a2c81b350ab62fe741cf179187f52abae111aa7bdf62449580872e2f810d`  
		Last Modified: Fri, 05 Jul 2024 19:56:16 GMT  
		Size: 11.7 KB (11693 bytes)  
		MIME: application/vnd.in-toto+json
