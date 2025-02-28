## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:e1976c8f5eb875d27d5482d8f6a8acfcbf6ded6e4842f98d865a87db5cbc17e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:01710340d47460ef1cc6a64940b502fb2c14a57dcf5738457a1fb7010fb01dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211082434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d740f60eb71a4f540ee3b81a59b3ad8477cb47f4f0b21526b9ce5e6d4d592c74`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7f0a890370e7b6290884eb8b70dcfcd6749f097764b13db947cdd9196f5b6ecd`  
		Last Modified: Wed, 26 Feb 2025 15:57:24 GMT  
		Size: 62.8 MB (62802042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66d3d6094d4cd397049fc185148528c5f88b7930cf9c66ee49252ee8239250c`  
		Last Modified: Thu, 27 Feb 2025 21:08:11 GMT  
		Size: 148.3 MB (148280392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b2b2bf4c3d19b9e3fc0d43fb42b3e027f976084dd61ddf9092ab197e796918d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5754ca9b91b9363f72a1e7883122f0a8dfdc4b0a1ae1c846b0548007f446643a`

```dockerfile
```

-	Layers:
	-	`sha256:bd0cb815e1b33f06d2f3a04610de751e95584c7c36d21f22977f5d76aae4c9fd`  
		Last Modified: Thu, 27 Feb 2025 21:08:08 GMT  
		Size: 5.5 MB (5524415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3f09bf3b98d6b1ac0672554c3828ec935ee57bbc93b3541260d4210764fc075`  
		Last Modified: Thu, 27 Feb 2025 21:08:08 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a61b165af814211ba830a12d970f0416cf61d844d72201424713b6be2e0d6e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.8 MB (209750028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6088f06786075404951e79ebf09a54475dc382ebacae4774b8cdd79f9e9918ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1ee6a520dfdd6812ef0dacbc83e55b94ed9d247f76cf836c1a627af00562f8`  
		Last Modified: Thu, 27 Feb 2025 21:10:52 GMT  
		Size: 145.2 MB (145228820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:75f7a2b5456fabb1a0eed5dcd04f366faf0547692df7e54a5569d94fb959ef9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a25cd4454af2c90eb96ca8231948d3c155969912a1d8073a86b6b3015aabe8`

```dockerfile
```

-	Layers:
	-	`sha256:0b00e444eb08b694bc6ac397f9b7003fd1d6708721bdb54f9126931f15300b51`  
		Last Modified: Thu, 27 Feb 2025 21:10:47 GMT  
		Size: 5.5 MB (5523909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c654c4281b629cca61b165462245841f700bd6c2bff45e8d4023eb3f9df07732`  
		Last Modified: Thu, 27 Feb 2025 21:10:46 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
