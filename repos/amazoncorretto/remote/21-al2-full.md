## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:5fb4bdc394b388bf681afb794e835e4de6e32e66c62438e192afb4ba1090eea3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dfd2918d72156262d91cd54ba6c1b64f2509f911e8a03383b0c0cde4a250fb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228427256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55edec46bbce73f57884b24cbc236a8015d39aff690fe5ce079cacd263df4c49`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:30 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:30 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:21 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:23:21 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:23:21 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfbb2013f839dc1b3c014b823b3aac80d0e6d67fac06ba1b5ce16eef96069369`  
		Last Modified: Wed, 03 Dec 2025 21:11:38 GMT  
		Size: 165.5 MB (165496684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cbd15a4fe4db637a12218d312d7ab8903a9c11c070d50661816f6a406337d632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3456aac882179cbfe98ff21d3fe6546ee79fa3bd4d0dbb0c0fdbb6935cc04853`

```dockerfile
```

-	Layers:
	-	`sha256:2f5ed5e3e1709a416802aba7633170de1168cc19eaae8939aefc80d23177d5a0`  
		Last Modified: Wed, 03 Dec 2025 22:49:50 GMT  
		Size: 5.5 MB (5535599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e01676039a67a3052a7a5b749bbd10cf0204c4f15e3844a3ff21ce1e420f1cb`  
		Last Modified: Wed, 03 Dec 2025 22:49:51 GMT  
		Size: 11.2 KB (11206 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fe9cf6dc4386c94c5126ea091133080dc6935363bbbb1161054378e99eff2c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228375682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae00be1b7b7b98946ddf80da98ce66fa40806c9fc6d1980951bab351b8ba0280`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:03:07 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:03:07 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:27:26 GMT
ARG version=21.0.9.11-1
# Wed, 03 Dec 2025 20:27:26 GMT
# ARGS: version=21.0.9.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 03 Dec 2025 20:27:26 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:27:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ba2b3f44053754feffb2ec7cfa45b66127e117d0d28e5607dbc6e1b6044b97`  
		Last Modified: Wed, 03 Dec 2025 21:41:24 GMT  
		Size: 163.6 MB (163582881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6ce96ac08ae945868bc58f58d12170fad181fd5d75844a88b62dfc22b8faac36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d046935894c98b4eb5b5ebbd4cb872f4b94d523333bfe87da07c13ce3a96cfdc`

```dockerfile
```

-	Layers:
	-	`sha256:624fdb07fc70363378f4a9a57b2cda89bbe161cf9f65daba6ccf77f20a4173ee`  
		Last Modified: Wed, 03 Dec 2025 22:49:55 GMT  
		Size: 5.5 MB (5534288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7468576e20e7d5149b1102f47cd8acd628ad7b5c0ce6d17663df70578ebdb0b`  
		Last Modified: Wed, 03 Dec 2025 22:49:56 GMT  
		Size: 11.4 KB (11357 bytes)  
		MIME: application/vnd.in-toto+json
