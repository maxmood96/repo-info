## `amazoncorretto:21-al2-generic`

```console
$ docker pull amazoncorretto@sha256:c822834af06f45fb263c9dc719e85954e101e8fb706f3b9bdc2b36fab3844341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6723ce6680234b7ef81480d5c862410e4e813ef1fa8a2f2ae525a8ec3d71334f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227472431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d62cbac096849a73621572d6cf3b972f6247d205fcb987d793df01258732e51a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:8430d4c5a00587f0a8dc4c62f82455c123b54b9016d43897ee77c496c018a8bd`  
		Last Modified: Wed, 06 Nov 2024 20:48:04 GMT  
		Size: 62.7 MB (62681042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405311cb2136ed981e05c69394b3b693dfe87afab98a57d48faeecd8d18d0a87`  
		Last Modified: Thu, 07 Nov 2024 21:48:07 GMT  
		Size: 164.8 MB (164791389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c213e126e2bc472cd17963a0168dd0dde2967baf9b40464c2817cfadfc23d342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6f6cbbdbfd2c537ecfee9fb66dcdd682335650ad37bf5a99ddd60fbc420476`

```dockerfile
```

-	Layers:
	-	`sha256:c7f1dcb05255d89d5f0e339e7f7f139fdf9b5d0ab14538414ef2945edb2dd7d7`  
		Last Modified: Thu, 07 Nov 2024 21:48:04 GMT  
		Size: 5.5 MB (5527670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e13c3de1b3d3255903643ef3d10b91fe0ffe92a4b5b39f838e9bc82d5903427`  
		Last Modified: Thu, 07 Nov 2024 21:48:04 GMT  
		Size: 11.2 KB (11249 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:157f9c925303f73718dc2c44571d60eb2db36ec77554e0c8aa3d6e31c15f4477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227429358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2943be9fbe66a6360fd65057d962007c761fca9a00348a1f598bf07b082e8c59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0a62aca1c7d7ec3e0e098bf23685d8f0fcd19e33577a91dafc6dd30bef06deca`  
		Last Modified: Wed, 06 Nov 2024 20:48:17 GMT  
		Size: 64.6 MB (64588571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5636d0fef96340fb04185b1d0e1f33327a11f95955bf2cc5ccf6b19483e3e682`  
		Last Modified: Thu, 07 Nov 2024 22:03:25 GMT  
		Size: 162.8 MB (162840787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:17ad82f3ea29483ee5e38bbc64cf27a718da2c51ab28a6536e0e81def1773655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5537758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc0bd77db2f6abb3a8c55bb9ce74db77af9489fb94d02157f441f205e3b62a8`

```dockerfile
```

-	Layers:
	-	`sha256:de5a9756460f7cdc85a541d8b946d8c5c467ee5bf3a104dc1b38c01faef50367`  
		Last Modified: Thu, 07 Nov 2024 22:03:22 GMT  
		Size: 5.5 MB (5526357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d9908933cb87afec92a5e452e433593cb4746db1547ff4ec1e6b50f059a4fce`  
		Last Modified: Thu, 07 Nov 2024 22:03:21 GMT  
		Size: 11.4 KB (11401 bytes)  
		MIME: application/vnd.in-toto+json
