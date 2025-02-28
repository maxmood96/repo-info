## `amazoncorretto:17-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:92262565df954763c1d183d8e56f80404f277466fb7cc6c06bff5f92ccf37b01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:94d7df9a5b5a44c05c9b085c9731d63092d5b0e63ef46207d248073ff7ed1038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214510661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1ad362c60552cd4be6346adef18a69c86ef4787250b5676008ade67fb9f702`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7f0a890370e7b6290884eb8b70dcfcd6749f097764b13db947cdd9196f5b6ecd`  
		Last Modified: Wed, 26 Feb 2025 15:57:24 GMT  
		Size: 62.8 MB (62802042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd80d9102693c028f9a17805e32a1ff6659cc05fdb307ace59ad2d0e346f5a8`  
		Last Modified: Thu, 27 Feb 2025 21:08:18 GMT  
		Size: 151.7 MB (151708619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aacb69573ce97a0d88955fd815f881eef990c5f7fdb4bffba37701f45cea16a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0ae0cb2d428237e9aab2a913198bee7de01c160dd946eb4a8f6e20b773178f`

```dockerfile
```

-	Layers:
	-	`sha256:94858f653c0028640579b5439161387148740667d6f900da0125e9bee9b3ea43`  
		Last Modified: Thu, 27 Feb 2025 21:08:16 GMT  
		Size: 5.5 MB (5517110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:166029f0d51e271ebfde3806104315cf658c8a4bbab9586942638f83ff767cbf`  
		Last Modified: Thu, 27 Feb 2025 21:08:15 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:494c7372eb54c74911ff18f8fa9ecbf6fc54b4b994fc15995b286130b3d487b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214774602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12cb5295628bf39bef5093edfaa6ce6ac2112c109c9a541f3dd825fe20a0e2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f3d00f7a4453c907701f44e7c57e8cceebb988daf9b801ee509585a530b051`  
		Last Modified: Thu, 27 Feb 2025 21:15:47 GMT  
		Size: 150.3 MB (150253394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7163cd537f501db580999fb305a0877740cf176c6a8258eeeff9ade11e6fe327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a17a1e708881c6adcc3d8a6d20c6ea915d473a4ec1c8e37683627170e9bd44`

```dockerfile
```

-	Layers:
	-	`sha256:9b98f3a25a5796fc9f544ec6401bd6a9e894845b06c763674ba0669fa55c3058`  
		Last Modified: Thu, 27 Feb 2025 21:15:44 GMT  
		Size: 5.5 MB (5515799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8a655acf3039608cfd01080abc7598625d500db5b57ee2dd6f26446cf4638cd`  
		Last Modified: Thu, 27 Feb 2025 21:15:44 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
