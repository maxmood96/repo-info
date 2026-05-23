## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:bd4926683c53b595c071cc7a5d0ee23e0f36b99a243715bd9556d2418399d073
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:98821b2f8e3db08262073e20b4007f68e9b6dba01b23c00cf6bef500bed09c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215622524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb783f36cf1a02f6882241caffc96ac0115be78f13d5f98d259117f802007aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:28 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:37 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:37 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 22 May 2026 21:11:37 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:45dd431b24e3561020a83f5e29dd2642d9ec2f2788c6826e5b1e9ee25ee38759`  
		Last Modified: Sat, 16 May 2026 04:14:19 GMT  
		Size: 63.0 MB (62951975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1c70d1c6953a128a159df107482ccf05c002cb93693078cb9080127ce0eeff`  
		Last Modified: Fri, 22 May 2026 21:12:00 GMT  
		Size: 152.7 MB (152670549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:14c7f2ffea155ae2721f682d28fcef3eeb74d1c15903f3743df0ae1ac8fffdae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5547830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f86b983375d7908985065ae242352bb3b31f450c4a45c38bc2b1b1ad5c6cc8`

```dockerfile
```

-	Layers:
	-	`sha256:9ce0861052e8fd429b01c8281d3fa73c37619579a852128f2c623604a749e0d8`  
		Last Modified: Fri, 22 May 2026 21:11:56 GMT  
		Size: 5.5 MB (5536617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec52ce91a85e8d253e2728ac5388dae4abba9d895eb11ad5021014609d3c9db`  
		Last Modified: Fri, 22 May 2026 21:11:56 GMT  
		Size: 11.2 KB (11213 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:01286242a8cc02fa9f19823a3b41ff5a069b48b6a49bdf03b04a4c4dea176b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.1 MB (216108397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b63969ab39d4b1f10cba742baa8ecf95f71ef734915334634370d63ebde8e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:43 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:04 GMT
ARG version=17.0.19.10-1
# Fri, 22 May 2026 21:11:04 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 22 May 2026 21:11:04 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9b55de233aca71116430038a4df795c9fbcd988648b5d3ff05692945d681a5dc`  
		Last Modified: Sat, 16 May 2026 15:07:44 GMT  
		Size: 64.8 MB (64790017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d876074273e0cd4b6cf1c24604ff033565872c6d506da1298267fccc360c96`  
		Last Modified: Fri, 22 May 2026 21:11:25 GMT  
		Size: 151.3 MB (151318380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fa86f3f9d06cd03aded992b64c66de5e562eb6cdeb44bfa320ff4d4997660fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5546671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c1b030f045896b987e3fa8cdc897625dd688bbcd32c171dcc66b31d012b39d`

```dockerfile
```

-	Layers:
	-	`sha256:b4aec002946eac7e217f7e8ea73946b350145ac5d962254dc28c158033e25601`  
		Last Modified: Fri, 22 May 2026 21:11:22 GMT  
		Size: 5.5 MB (5535306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f8b6b05a150c4110284fe5231b7df678b7cd83268a3270b9cc4bc630098cae`  
		Last Modified: Fri, 22 May 2026 21:11:21 GMT  
		Size: 11.4 KB (11365 bytes)  
		MIME: application/vnd.in-toto+json
