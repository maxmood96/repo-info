## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:6e7487368a7b345d24345fcac7f73f4ca6fe75ca74fdeed2e2ef37ae359cda28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c4f41b9d0be24686c0e1836e9dc12cd495b3d960ce73be2c2c4812fe4d801769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228488819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5394e8dfd6ca0c2762cf4388cac14938f44669bda6dcd274b0f272979cf83d3a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:01:02 GMT
ARG version=21.0.10.7-1
# Wed, 21 Jan 2026 19:01:02 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 19:01:02 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9734ae141deadfb5277ec23e6c24e8976f7bb7a64adc73ca3a463a3787f6a9`  
		Last Modified: Wed, 21 Jan 2026 19:01:23 GMT  
		Size: 165.5 MB (165548663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ba41b84aeaf5eb19e57a6b66d01519eed7e6b2d37bcea0691670b17ff85893bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002dea026628e358d687090f8a22604a3815408ba0943194e0da7fe178b12695`

```dockerfile
```

-	Layers:
	-	`sha256:300e54417977113635edf45c035dbcba20c0248170383079f08153d829a0d4a6`  
		Last Modified: Wed, 21 Jan 2026 19:51:33 GMT  
		Size: 5.5 MB (5535607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c64fe10d3c8e121a351ae4127631e33b6a21b5971a117ee297da82b1ff9254d9`  
		Last Modified: Wed, 21 Jan 2026 19:01:20 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5b5050fd26a43ed03d2f0732cec18b95e629e1b2de9f4e5b2feef2b1625a3d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228378186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df348df1cd709e6d9281540cfda219643b3e75d140c96138aa355f6a1bba6e7a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:01:10 GMT
ARG version=21.0.10.7-1
# Wed, 21 Jan 2026 19:01:10 GMT
# ARGS: version=21.0.10.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 19:01:10 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 18:33:41 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c644fd68ad0ef8767143fb9c719ddfdc169e6b7ea10b4fa2eb80955461cd3f`  
		Last Modified: Wed, 21 Jan 2026 19:19:19 GMT  
		Size: 163.6 MB (163607752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eeb9b27fe13b520b8f64eaf79f321752f368ef44bf74a3041bc72e03bc0bd2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab373718fdf901559b9df5b448598d7485b186afb51b6f346886a3f3a429dd6`

```dockerfile
```

-	Layers:
	-	`sha256:a7ae4312d8b4d5362d4cf2b713243b2d4d84e41f25f379e064a87a9df7a2ec71`  
		Last Modified: Wed, 21 Jan 2026 19:51:36 GMT  
		Size: 5.5 MB (5534296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf8f857068c6fe4417051568e4730f38de40f955e91d354898220470cfefd964`  
		Last Modified: Wed, 21 Jan 2026 19:51:38 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
