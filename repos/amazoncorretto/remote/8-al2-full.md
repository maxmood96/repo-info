## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:063fad410fd966dc15c8c57379760e1295eabd46d49048fd180d1022c3e69842
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2ad0b5071b3a9d3279997cd3a0943d0c5ba3ecba9b9e258d49f924e4268aed3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138977973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa45d0c1bd23c783dda5aa5477ebae178d80ea69005aee1ef28a9aad1a48cfd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:10:31 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:10:31 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:10:31 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:10:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f169c4ab9c5b596302c6e78d09dc97ac1a459af646782f43c571ba613820`  
		Last Modified: Fri, 31 Oct 2025 00:11:11 GMT  
		Size: 76.0 MB (76043905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:13c0580ddf23a20302e42ba1ba0a4345453d6fa6a95276bc112fa7e0a6e1ac4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfab13b11e8a490aa4f69fb2ea2ebb2b20e453cf1337631d6ed21301b92c3137`

```dockerfile
```

-	Layers:
	-	`sha256:9e4203b90952f347656d668b1c71fb636fcb8d503b1751eefd883fce1c233706`  
		Last Modified: Fri, 31 Oct 2025 02:21:03 GMT  
		Size: 5.4 MB (5377354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:778adad670557da6f9be0bde2816626a8ca26b98407a0c94a3b85a121ee4f1e1`  
		Last Modified: Fri, 31 Oct 2025 02:21:04 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5ecd7b83dcec33c751bc64f515a4f15afcbbf2388fd471242b8854bb75bf3d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.9 MB (124912376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e463a7eef497149ebae06aadaf9952ce5693d310c9d63ef879a6a1b0ce9b49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:10:58 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:10:58 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:10:58 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:10:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d96ed5cf7cdd43c028ca3ffb2b3c794c53305e80d242b1a23649bd6d4c7ac`  
		Last Modified: Fri, 31 Oct 2025 00:11:39 GMT  
		Size: 60.1 MB (60118918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:338a5d4aba6c8c1692a7242bc53f340744f2ed0b53cd60f0ffb2fdbb444e2288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8d8b87d4a6537d593edb82bc55d47c47bbeb658b7c2470e24b5039a69c32f5`

```dockerfile
```

-	Layers:
	-	`sha256:896d9e75f55d7c83bdaa61ecaab4c2149d147bec22617503b641b611469c09fa`  
		Last Modified: Fri, 31 Oct 2025 02:21:07 GMT  
		Size: 5.4 MB (5355853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:095d53c0d33633d5b91988f50fc55bd4b5cef65b2b3f7a3dda9fed4dac126978`  
		Last Modified: Fri, 31 Oct 2025 02:21:08 GMT  
		Size: 11.7 KB (11691 bytes)  
		MIME: application/vnd.in-toto+json
