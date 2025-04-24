## `amazoncorretto:17-al2-generic`

```console
$ docker pull amazoncorretto@sha256:f9a357fd7c321bb706a05725e4f62f229394a77d4747e30cd4efa370aef5f888
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1b6f4d06524d07ba9f6bf0e286e592a7177c649d159da582728520a8b2a3a045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214540511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11dffaf10df8739682ef9fe13bf637861d57576e0d488d7d306b5930f7f033b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:07f9ec6a4553009171ec20ecdc638afd0eaac432b31f9e1b569f6e4fe9454d93`  
		Last Modified: Mon, 21 Apr 2025 21:48:34 GMT  
		Size: 62.8 MB (62761722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f431f62e4910c564957b32af7d7dbce3a144835c6e7ac0ce5555ef33f39ebba0`  
		Last Modified: Thu, 24 Apr 2025 20:08:06 GMT  
		Size: 151.8 MB (151778789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:78877bc570872e4f4ea10513c9e4caa3c592033262f010297738c9312f834089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080f22dca65cdf0cdc3abf384f10be6788e6659982aa3e1baec87f7130859c6b`

```dockerfile
```

-	Layers:
	-	`sha256:849d45b4e7ffaf7bd7076f66e5da2bc333084022aec66e6fa566308869bcd081`  
		Last Modified: Thu, 24 Apr 2025 20:08:04 GMT  
		Size: 5.5 MB (5519012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:102741b48a8baf3531f75fefab2012e653a550b094554938717923a90c1f9cef`  
		Last Modified: Thu, 24 Apr 2025 20:08:04 GMT  
		Size: 11.3 KB (11254 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0011a234aad2575fc434b7ed17cb99c2679d4ba1a1a06cbee0864af2092a579f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214949932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4bf1d871cec0dee738ce9d4234a4b2f71d9491248cb5f1104bb3e38db49631`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc78a794204205caf229722289ea3beec64dfead5533793f7446dc927d5a3ea`  
		Last Modified: Wed, 16 Apr 2025 00:08:14 GMT  
		Size: 150.4 MB (150384110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:24f5b1056593318d4b784841e324591c5780575490c5188decebeabb9010b01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85040540e5eb07f8c2b32808e1b6623fb6cdfb4225df1e3b4a5f0b656e279add`

```dockerfile
```

-	Layers:
	-	`sha256:52b3abb417c86f005161d1e89308e8d4e2c3b944af1e7faae58bba6f2d1102d3`  
		Last Modified: Wed, 16 Apr 2025 00:08:10 GMT  
		Size: 5.5 MB (5515823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859cca0c9ebe4f7f3360332e6415105e97465bb1d20de216936b695edee189a6`  
		Last Modified: Wed, 16 Apr 2025 00:08:10 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
