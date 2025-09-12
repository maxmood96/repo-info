## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:f408b1726a70dc7e4daec23959a47d4464d6d962e8e1f756dd1b42f73b139cf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ddf5c046f7e6c7a8619ad7ca556813e4f302716f2581ff1aabcf40a83d440243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138640206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f845a632be3832bc45211aa52a6b83abc18ea386273cc76ae69f87679f040673`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0c31e84362b17be00ccd03302ca56ddbf8561b17d46e8c82bc87c21d389e7731`  
		Last Modified: Mon, 08 Sep 2025 20:24:26 GMT  
		Size: 63.0 MB (62983288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1206d1a527bf97207bf92f07c8d19d27a926f631b1e78c826443e2fe01c9ea5`  
		Last Modified: Fri, 12 Sep 2025 02:09:53 GMT  
		Size: 75.7 MB (75656918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0a38ae056cd13f783b6950494d87ab3098ac3e11a10c1d0f73a35ed9ad6020dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5386500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240b3141385973c1b5ecb60aebd2a19ab4833eb0ea4dd9822501e7406a193984`

```dockerfile
```

-	Layers:
	-	`sha256:bb2d3d92ca2883d4cc84b010b0569b4e0cf5916e3f1c4a4e91a159cf34683e83`  
		Last Modified: Fri, 12 Sep 2025 03:51:35 GMT  
		Size: 5.4 MB (5374931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23be70c376d35556dc87e77f9956ebd791f920f8af98384c227adeff0e19ed04`  
		Last Modified: Fri, 12 Sep 2025 03:51:36 GMT  
		Size: 11.6 KB (11569 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f1faca17f1d5805828a21f9ea09cd148757f07f171c7552833325cbc67a205dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.5 MB (124455082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01cdb72e8c05027914596805537563dec8a1c636b2c5808a440746fd53d89b27`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:44fb931604a5509dd2f5cbf8d1604d64dd0f56962f61bf6cd3f092bce2e7687a`  
		Last Modified: Wed, 10 Sep 2025 17:52:55 GMT  
		Size: 64.8 MB (64791723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a98df12e79d218dddefadd11fbdc1910e53c6818057325cd488597efc67a9d`  
		Last Modified: Fri, 12 Sep 2025 01:11:07 GMT  
		Size: 59.7 MB (59663359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:516248f73c81776fc1565db0baaf62f5b86bdf13776a2b42db62a20732443333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5365164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eddf27fb648c10b9ce9e5b0e94adcd0b79bce9192670e20cccb88878f3bc6bd7`

```dockerfile
```

-	Layers:
	-	`sha256:0c618210bf8c207f54788daeb810b8e570198bb17019b884852e7c24c9e2d709`  
		Last Modified: Fri, 12 Sep 2025 03:51:41 GMT  
		Size: 5.4 MB (5353430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baffbdcf89622950151da2082983b83847bc55cb30d6932ef047c55bb8d49ef4`  
		Last Modified: Fri, 12 Sep 2025 03:51:41 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
