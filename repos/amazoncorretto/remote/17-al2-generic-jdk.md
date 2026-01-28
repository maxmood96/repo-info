## `amazoncorretto:17-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:c4068a14fa577c34e05a5d3049946b8eb78ab410ac90a27459c4e94acbc0ffb4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:388a9e58b62bf32ecfdcd24d9b23d7b239f16fc6a33af8894d801ddc2cb662c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215430427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf81109c2f500da15871f6351353f9bc6c67948fc6c3360c8e7d3e8de1def23e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:03 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:07:54 GMT
ARG version=17.0.18.8-1
# Wed, 28 Jan 2026 04:07:54 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Wed, 28 Jan 2026 04:07:54 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:07:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a2d2329696ab8b0c3dedbef26f731c98d73070e27c55d70a9b087cf07aa391d2`  
		Last Modified: Fri, 23 Jan 2026 08:54:27 GMT  
		Size: 63.0 MB (62963709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2e97d73ce2dcd3ddf3ca49bd76b8633f971d0ff9f5086086e3467c49d62b5d`  
		Last Modified: Wed, 28 Jan 2026 04:08:15 GMT  
		Size: 152.5 MB (152466718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:043406cd4e24d0e0dc68f7460ee2849668f22527fcc9f3515fa0a38f7dad2940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6025ee860253263b35a6f2713ab0c11dd4d926859cb2583279db9e52d2dbd24f`

```dockerfile
```

-	Layers:
	-	`sha256:d61a5b696bb520c7a69e94b37cc4bce2d4140e35e8172d0b6bff79bcc9581d9c`  
		Last Modified: Wed, 28 Jan 2026 04:08:11 GMT  
		Size: 5.5 MB (5535704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7899c0ea00c3a3d8783b55ee656f5e9542039d70db64e28bd947c009fe50189e`  
		Last Modified: Wed, 28 Jan 2026 04:08:11 GMT  
		Size: 11.2 KB (11211 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d597e0a2514f0a6e84641df7d29a852bcd64215669fa0bea71996044e46af172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.8 MB (215776494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf56b4494e832f8eb159445dd66034ddba375ff782401bf720f69fc53b924d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:20 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:13 GMT
ARG version=17.0.18.8-1
# Tue, 27 Jan 2026 22:12:13 GMT
# ARGS: version=17.0.18.8-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 27 Jan 2026 22:12:13 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:82c5a31266c8bcc92344bc9be0616aaa6ddec6433baf7a22403b54627046c283`  
		Last Modified: Fri, 23 Jan 2026 13:06:13 GMT  
		Size: 64.8 MB (64798889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefcca91c46c186fe23ce434b50d9455a9fcceed3632768e2013f9ac8703212e`  
		Last Modified: Tue, 27 Jan 2026 22:12:33 GMT  
		Size: 151.0 MB (150977605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a14980539035028ceeb8c9c2403aed5e41d8dc396d9732a95faebe12cf935879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5545756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6a50a5d9d2fd4814b4b9ebffc114b2395a6b452d6eb2487c1a38c1e68228ec`

```dockerfile
```

-	Layers:
	-	`sha256:5086b534233f7847c2296583cbd2a4a17d9b272cda5a7104f28388b237f86d91`  
		Last Modified: Tue, 27 Jan 2026 22:12:30 GMT  
		Size: 5.5 MB (5534393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff97733794539859079a57ca1156f4d511bab04bebabb0f681bc7343d50282e`  
		Last Modified: Tue, 27 Jan 2026 22:12:30 GMT  
		Size: 11.4 KB (11363 bytes)  
		MIME: application/vnd.in-toto+json
