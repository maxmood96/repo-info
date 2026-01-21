## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:37431b219b2d435ec102127f16612593183de22759630f77f264abacf6e5f60b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ba0ad1c36eebf7691a531650656c9aa6928ab502d783f3bc6247599b5ed2df9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215403091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862168c725f20c067148389c333a99049c977196b217bc8809ce9c8d485517e0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:15 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:15 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 19:00:15 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:23:48 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d09c36562c02e291fec0cd8d510ab0c206591e85dce9cebfe7fe6bd12f6006`  
		Last Modified: Wed, 21 Jan 2026 19:16:44 GMT  
		Size: 152.5 MB (152462935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cf004c8302859384f7423b809f0fdf1271d792e64bce3d3089605f8522e0fdec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba6aa066535816d9b91385119a852905b14bb4b005252c1ade3ff1b10b61a05`

```dockerfile
```

-	Layers:
	-	`sha256:00627c2e2e25ea22d3f54f42aa6a63af34ac48cac776138e1a8e98252ee000a5`  
		Last Modified: Wed, 21 Jan 2026 19:49:28 GMT  
		Size: 5.5 MB (5535704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d0f94eb27fa4b21689be06e93ea7b5b0b8a6b704dd5fbdd95db0030d716b77`  
		Last Modified: Wed, 21 Jan 2026 19:00:31 GMT  
		Size: 11.2 KB (11210 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2f01c3eed80c8ff1ece4c7dafdb8a206141726c944f5d6eec274b6c90c7ad103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215755576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2f89aa3ebe5e5cdf9dc7292512704205d3003b53f4598d0b0560ee072a68b7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:00:16 GMT
ARG version=17.0.18.8-1
# Wed, 21 Jan 2026 19:00:16 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 21 Jan 2026 19:00:16 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 18:33:41 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da03988e890a2734422b08930678b55aacec1ee085bede5e1b18f8c3f898b33e`  
		Last Modified: Wed, 21 Jan 2026 19:00:37 GMT  
		Size: 151.0 MB (150985142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5ef2aa77625cc1eb2a2a99ba0f91be5b4e6e969bf70570577ddcfd196a4a8bb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2426b421ef17f664209ed9f876b23d95a167e884d04294957adf0c23f156a535`

```dockerfile
```

-	Layers:
	-	`sha256:22756e278f145575f8c177d90579030c54a1e96b77924911ebcad7509a6ff4aa`  
		Last Modified: Wed, 21 Jan 2026 19:00:40 GMT  
		Size: 5.5 MB (5534393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56be37c9baac6eca30022a1fddeddbcc240b0d3457454810d33c9e379b5dfa17`  
		Last Modified: Wed, 21 Jan 2026 19:00:35 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
