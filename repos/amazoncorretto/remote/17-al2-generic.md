## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:aa2d8a673168a46827c1388923272f5d9f993a30d4154fdac2cc34392d845140
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:da565cfd0f8740726da2034169d89a604ec60da287a3ef10a351ed26dd58b817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214918638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b567821d186b893f9e20c99b761274f6ad9ed12163eecfd7409074aaf241151f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df11a0c6fe6598f14df2c6965839731eb386ce402d5fe099502b34e9f5415f9`  
		Last Modified: Mon, 07 Oct 2024 23:59:59 GMT  
		Size: 152.2 MB (152240482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:288f4241aa5777eebcfe2a1f8a317bb24a9c809e1c8ba8ad920823a771235d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa3437fe4da9fd3d1fecb1d76f11342eb7958bc4f17466caa50fcb7ed1da14da`

```dockerfile
```

-	Layers:
	-	`sha256:6deecbebf2bc34c94ca33cb9f7973a2c9beb411b8707b403734977fc835bd724`  
		Last Modified: Mon, 07 Oct 2024 23:59:57 GMT  
		Size: 5.5 MB (5526967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a88a61efee98546183e898ee5736eedba819e3fc043468ef60a2a93bdc87383`  
		Last Modified: Mon, 07 Oct 2024 23:59:57 GMT  
		Size: 11.2 KB (11226 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7f257e1988767e61a376947cc1c6df978ae7001b559c33d88f6b4f2c20640e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215459978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d27283dc6984f3d625dd5aaee2509a7793fa2d2f78f7857bb1c53e40c544e77`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=17.0.12.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7299208573fc69f06936b225767fba87fe52472780ef2a2a0cbe30f27997d017`  
		Last Modified: Tue, 08 Oct 2024 02:03:45 GMT  
		Size: 150.9 MB (150867319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e27a2706287736928501b1f7f6a2ed86cc733f6a2dfae87510b481218d3c247b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7529131a4d5e871b9fb3500d6cfbcb8265ba5ffc65aa9018e09a4b96c81528`

```dockerfile
```

-	Layers:
	-	`sha256:ec65eee131334d3e0753d9883dd3ab232340ede90b3d4bd9c608cff7f5339fac`  
		Last Modified: Tue, 08 Oct 2024 02:03:41 GMT  
		Size: 5.5 MB (5525654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677141d95d4b4441d62ab60af62d95505e5153ebced28b92b99da8506b1b0db9`  
		Last Modified: Tue, 08 Oct 2024 02:03:41 GMT  
		Size: 11.4 KB (11377 bytes)  
		MIME: application/vnd.in-toto+json
