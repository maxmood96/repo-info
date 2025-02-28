## `amazoncorretto:21-al2-jdk`

```console
$ docker pull amazoncorretto@sha256:aa94fda5e3ea59687d0a68e1c491687cb9d7365245d077684f848b2a53f1430d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cae0ffa0cceecfc39ce6a1e9e8a22a45fa7909a6917961a6617dcf63ce30224e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.6 MB (227626958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0904f7323421667168e9617fdb42abe1a47ff4e7fc2a2929405548eba644b8c9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:7f0a890370e7b6290884eb8b70dcfcd6749f097764b13db947cdd9196f5b6ecd`  
		Last Modified: Wed, 26 Feb 2025 15:57:24 GMT  
		Size: 62.8 MB (62802042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e99052b5e7643753b8d685cc1e05b03ab620d534005c9c9c5d9560fed12777`  
		Last Modified: Thu, 27 Feb 2025 21:08:20 GMT  
		Size: 164.8 MB (164824916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:817faa553bc734803b57b581656ea23927084b2f00ddcc7e3f45a7075aff89eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7ad0bae7cd892b952c237ced43df5c1970ded0345962d51c276f249092c903`

```dockerfile
```

-	Layers:
	-	`sha256:05492a0d006553221ebebacca6929d0457c373354cf5a435b8c8d125c9d9b6b1`  
		Last Modified: Thu, 27 Feb 2025 21:08:17 GMT  
		Size: 5.5 MB (5517001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26f90af5ead5cabc80c63496c0304b3e4a24647e1277c8232ff4101ee5383a2d`  
		Last Modified: Thu, 27 Feb 2025 21:08:16 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7edc7f3ac14dda279516553e64cc83e1266273844635d3e888803f10de4e8024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227331908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dd983d70c9d30139322d10f2bc01393a5c146b406a9f461a9a35db5aaef7a62`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9033b51658d3a3d4c550c89424db4382b2da4dfd6525286c8e303377d9c05bce`  
		Last Modified: Thu, 27 Feb 2025 21:21:38 GMT  
		Size: 162.8 MB (162810700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ffbc751421b0758de5d3d908a78a063df04306aeca5ac3bfc2957106897a34a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25e847f1ea7c6af60c33701f86f9c1884e2efe7580516c8727cbe6370fefd9d`

```dockerfile
```

-	Layers:
	-	`sha256:95ed4a3799914bf0057376585b6333477fc05e27714ec637932bec47c89d9a3b`  
		Last Modified: Thu, 27 Feb 2025 21:21:34 GMT  
		Size: 5.5 MB (5515690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6baa0a0e60d4b24fea4ee38ea173a66a6b50044ba3744040db9ada4a97e4f9e3`  
		Last Modified: Thu, 27 Feb 2025 21:21:34 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json
