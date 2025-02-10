## `amazoncorretto:8u442-al2-generic`

```console
$ docker pull amazoncorretto@sha256:c1d823bc44147cff855eb0c2f9985bbcc40a7383ee4410d0624fefae76a3988f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fe280759af0f1ba8093d77ddde53cd633e65fa5108f0a4c42693cc247227a355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138219394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafb4105e72bfd9a6f7b60e1d20a25e583cf8fcff2883ee067810fe5d266b529`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:43fdf45428917f1f386fbfe0eba1ccfdadae7696a4cce30a96cca587ab25ab90`  
		Last Modified: Wed, 05 Feb 2025 10:24:14 GMT  
		Size: 62.7 MB (62665244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4ce21139298855cef0fff8868fbc42223b7e837149d4b70f86224b1ab276c6`  
		Last Modified: Mon, 10 Feb 2025 20:08:27 GMT  
		Size: 75.6 MB (75554150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c13728ac9663da0edb962d315e5dbe197a6204406740825a405112ef7f653693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f010e3bbba7c2afcdbb541cab240469bd3bf53b9a5cfe7ecf5b55b73e94fedec`

```dockerfile
```

-	Layers:
	-	`sha256:803294db1d7ae3d5905c0d1d2a4e47bd6b75fd73723f083b0717d383f3c40123`  
		Last Modified: Mon, 10 Feb 2025 20:08:26 GMT  
		Size: 5.4 MB (5359568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a2af42b9b1751538ba54893f7fbfb24b2fd6a94ec16cd05756326724d30bf2`  
		Last Modified: Mon, 10 Feb 2025 20:08:26 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u442-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b600bf34cb9bd5097e626cad877d10887bd65e826583133991e07251916e7de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124240847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafd36ffe89f7593d436328aa9f2a97c94671c77c12e805b23bd33d51acd5aab`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:e42e49097fe754943ed2309e7c2ac45f6631e5c57fa3daa55479809dc243c87a`  
		Last Modified: Wed, 05 Feb 2025 14:56:54 GMT  
		Size: 64.6 MB (64578222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2841449421858c24f162dce589a7a25d026560c97714e2d9454803961ba708`  
		Last Modified: Mon, 10 Feb 2025 20:12:02 GMT  
		Size: 59.7 MB (59662625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d245c0c7b6d09d7237c01b01a8cbc1d79d94229763318c859c99f8b3e3940227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781fa8e3441867e81469c3a7f4ff93d93cac1bddc7e3cbdb6e7bdceda52562f9`

```dockerfile
```

-	Layers:
	-	`sha256:f3e58dd4eefc09d64d87d7714e4178743df61605db1811a936851ff77329f2d4`  
		Last Modified: Mon, 10 Feb 2025 20:12:00 GMT  
		Size: 5.3 MB (5338067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad725ff3087982b7784efd80e51893b2716ae7f0dd08daf5203f84ba62c3762`  
		Last Modified: Mon, 10 Feb 2025 20:12:00 GMT  
		Size: 11.7 KB (11733 bytes)  
		MIME: application/vnd.in-toto+json
