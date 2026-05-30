## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:baf05acac731cdf8d5b3e400a89e40b7a161c558327009d6794ad057b386a7de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c529e24bd8ba92ba440a2dd6b181264da26ebffeefe3b60c8dd7d56bcebcbab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139056459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49bbd320cbdb126f4b53154c957ee4a256b9c4dce22848354176b83fccf1cfe8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:10:18 GMT
ARG version=1.8.0_492.b09-2
# Sat, 30 May 2026 01:10:18 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:10:18 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:10:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf014bc5c79b2f534d915f84aac636fa5ebd127f2eea997472261c971c4bc8ed`  
		Last Modified: Sat, 30 May 2026 01:10:33 GMT  
		Size: 76.1 MB (76114509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:415c556111a31579e52210f0d6de37950332b76ad656adf1fc5c84e0d1d41db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5388982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45883c374f2f6222aa02c69c4b754098dbca5899d4bbecaec7665d11eaf8de1c`

```dockerfile
```

-	Layers:
	-	`sha256:8ccb9fcfc6c06588148ce8ec23008770b036eb81d2ac4cf911c3aa31588b2874`  
		Last Modified: Sat, 30 May 2026 01:10:31 GMT  
		Size: 5.4 MB (5377455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060277645261d253e6c33cf289f36795462a743907f91fff3ae4a1673c83601e`  
		Last Modified: Sat, 30 May 2026 01:10:31 GMT  
		Size: 11.5 KB (11527 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:de8a9fb59ab6d5184bb47d54b73db12a9cd8489d6209db2b17f379890a3849b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124738666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c55465084bdaeecf52d44165befbed27601a0115c3d1b2c809dac33c7c1567e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:10:19 GMT
ARG version=1.8.0_492.b09-2
# Sat, 30 May 2026 01:10:19 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:10:19 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:10:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cdab7eeb22e07597e24f8d98c9bb7b21deae088a4ffb5ab1a8c89bdd3e7cf72`  
		Last Modified: Sat, 30 May 2026 01:10:34 GMT  
		Size: 59.9 MB (59947957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b31a09a40136b5d1594904f0671cd408ca68bf1190e7f97a58ac32ef9b3480c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de750690e1be2d601f2d2216c0b36daaeea1037fe8c83d562b175b190f78c01`

```dockerfile
```

-	Layers:
	-	`sha256:1182869eb80411ce783686b3e1a849950dc3028d75f730bac75454b951e6cae4`  
		Last Modified: Sat, 30 May 2026 01:10:33 GMT  
		Size: 5.4 MB (5355954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da71eae68fc7eacd1d321d588bbac2e34d63b58b2c52ae297470bee8077503a`  
		Last Modified: Sat, 30 May 2026 01:10:33 GMT  
		Size: 11.7 KB (11689 bytes)  
		MIME: application/vnd.in-toto+json
