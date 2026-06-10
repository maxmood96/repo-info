## `amazoncorretto:11-al2-full`

```console
$ docker pull amazoncorretto@sha256:4c5be387478a9fb419496c47cb07865e8c6d49af7db40f831b05256183122d06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3b64355b343f1ab1395d1e55ef8960892e3b24222bfbe0bc4a413600cdc6e1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.1 MB (211139663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:855a70ef94cf99d29f176accaa73167eb181c6005527a67f6879f0426c8412c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:26 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:13 GMT
ARG version=11.0.31.11-1
# Tue, 09 Jun 2026 21:11:13 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:11:13 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340f788e3e4c9f2421a1dc74f13ea633e946d05b3c439a603b63ec4bcd2d9b5e`  
		Last Modified: Tue, 09 Jun 2026 21:11:32 GMT  
		Size: 148.2 MB (148197713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5cd4a72ecd47c9908a79503b0bd3434d44ccad5845901418b3b06bef9e2ca81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5554322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d02bd3e46c902bfceee91a3c204dd44e93702615c70c6949e1be1133ecc43e7b`

```dockerfile
```

-	Layers:
	-	`sha256:5fd6848d0fe9b62f5dadae32ae796ac5e478c1ad0f7e96bd79e3d32949f37408`  
		Last Modified: Tue, 09 Jun 2026 21:11:29 GMT  
		Size: 5.5 MB (5543110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efe9ba5a4ef5572ca485a8e7d2564104ffa349bd5ffe00d81dd53400bd27b4a9`  
		Last Modified: Tue, 09 Jun 2026 21:11:28 GMT  
		Size: 11.2 KB (11212 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cc9526eaee34904c5821dffdf5140be9f83a6bcfb4c4cec30c3608fac3d750a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.2 MB (210165061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8231635a049f280363118ddf4c6a1722780210080d905e608c937fae5082253b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:22 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:10:56 GMT
ARG version=11.0.31.11-1
# Tue, 09 Jun 2026 21:10:56 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:10:56 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:10:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674338f6f96723415ae45000e59058e0a3106bfa1c91f82ecd657ecb6b3bc192`  
		Last Modified: Tue, 09 Jun 2026 21:11:16 GMT  
		Size: 145.4 MB (145374352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ba691a85a676e447048562f7735ff7eef41648aa7e0f27c00b0310eb8288ac6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa24445cf3675fef97f9478c17bb1231af84f3ed93c09e6b1805e1d61f2c3120`

```dockerfile
```

-	Layers:
	-	`sha256:9d173e1a4f5af2d470b8b97d4cd4be101d281262471deaad6b8b39f201d0ded9`  
		Last Modified: Tue, 09 Jun 2026 21:11:13 GMT  
		Size: 5.5 MB (5542604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84968be5edef1b7b351a8222807912afedfbf5c345426219896c684f33ac45b6`  
		Last Modified: Tue, 09 Jun 2026 21:11:14 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
