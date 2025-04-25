## `amazoncorretto:17-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:9cfefd0abf04e454c1c79d4acfaec95e10b7c315094ed7c79cd227db19f4ee20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic-jdk` - linux; amd64

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

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

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

### `amazoncorretto:17-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c49c20a256c906cac45291e569c6d2d98862e20a690ae5d83b070ec365a5a8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (214950977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c2f33d7fe258123dddd179acf43bbbff57ee1adf58d09610004ddfa6ae0b49`
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
	-	`sha256:928bddcbf112315a029f894cf829df2ae1b28c89ecaa6c142e3d47e62c803337`  
		Last Modified: Mon, 21 Apr 2025 21:48:49 GMT  
		Size: 64.6 MB (64582610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc501f322bde852c32915c6574fb1f947bb9346957d680ffccf06d7754031e1`  
		Last Modified: Thu, 24 Apr 2025 21:15:49 GMT  
		Size: 150.4 MB (150368367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8a9d198ef2a05a4de91504e3319a62613be3efdd34f3bd89fbfeee466ca88565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5529108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316a153a7f4d864401a09adf72bbfe6f8134f354d168e228fad5a2e5645b3670`

```dockerfile
```

-	Layers:
	-	`sha256:7d1c90edae037bdec27a42aed9def31a133e85b8391a2492fb72a50d3d19e119`  
		Last Modified: Thu, 24 Apr 2025 21:15:45 GMT  
		Size: 5.5 MB (5517701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f5d3ba6498b9b150aee53717a26cb3719b55a0f0cbc0e03cf6292077d6e254a`  
		Last Modified: Thu, 24 Apr 2025 21:15:45 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
