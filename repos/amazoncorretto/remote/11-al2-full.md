## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:317761a9f42e5707592068e50855f07e1a6e65d22ddb5e50176abdc1c1fd88a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:23b1d8423afebf5038c17ff03046021695a1dde42c3a2779e022cac162128ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211086451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddf5e7abfdc4a46e5e3794fe3c01431bc981c86846fd918670af0c3bff123a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:26 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:10:42 GMT
ARG version=11.0.30.7-1
# Mon, 02 Mar 2026 23:10:42 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:10:42 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:10:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:369d025c034936d3f19b9a4b859b983f355f304e2e95b16c4cbeb64c69d301c0`  
		Last Modified: Thu, 19 Feb 2026 18:52:05 GMT  
		Size: 63.0 MB (62960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9974138a294e9bce34a372ddf75b212ceab04f3897e26825c07edb81ae0510de`  
		Last Modified: Mon, 02 Mar 2026 23:11:02 GMT  
		Size: 148.1 MB (148126222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:be61185c8fcf315f491129463d98c4e6f3c2a99002aff0289e18f664baa5e46b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c21f48e6acee8b1de2ebeb2a2b837b83c27b8896bec424be454d922e4cbf21`

```dockerfile
```

-	Layers:
	-	`sha256:1a8bff369f58b01df5d58205221e18cfd06f3919eefcd4ecd6eed0d4613b2647`  
		Last Modified: Mon, 02 Mar 2026 23:10:59 GMT  
		Size: 5.5 MB (5543009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cedfca877e540e66952d70672c04dd675b73a7efafdd5f4f9baab16d767e7544`  
		Last Modified: Mon, 02 Mar 2026 23:10:58 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8dd515edf39a4026d9159b9b02225edfb18bacd86c218ffa07356f02ed62d46c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.0 MB (210028046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a496eb010f11116c04c9de973afc7ad65f6cb5f3870798013d436ffdd8b35221`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:30 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:11:40 GMT
ARG version=11.0.30.7-1
# Mon, 02 Mar 2026 23:11:40 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:11:40 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:11:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ce260c9faa157afc8e59fa056130319824fd1c549b337649ecc964c38a8d7b19`  
		Last Modified: Fri, 20 Feb 2026 15:17:29 GMT  
		Size: 64.8 MB (64811411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f33ac7713d32fff3dfbcd7dbaa1fd868642b368099b0721a9848c9e836fca72`  
		Last Modified: Mon, 02 Mar 2026 23:12:00 GMT  
		Size: 145.2 MB (145216635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:92f9a01a4883d33572f1125bd822cfda386e546f9810e817de90cd60b87906cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b7c964cc7875650251082215e446137d9e141db6f1654f2c8515320a130b29`

```dockerfile
```

-	Layers:
	-	`sha256:5e700ea10606c8b88feeee53161260714ff7928cfec0b0d04df5fc7053a06e3d`  
		Last Modified: Mon, 02 Mar 2026 23:11:57 GMT  
		Size: 5.5 MB (5542503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8321f3894e3499737ddb093367b596c4276964263470c9242a6d74ec26a4ca97`  
		Last Modified: Mon, 02 Mar 2026 23:11:57 GMT  
		Size: 11.4 KB (11364 bytes)  
		MIME: application/vnd.in-toto+json
