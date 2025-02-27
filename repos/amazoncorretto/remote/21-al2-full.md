## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:0c55f0d87401a7532f3010e89b9ac1be42796d388e043c771a7e4235e67f955e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

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

### `amazoncorretto:21-al2-full` - unknown; unknown

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

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3bb30806b3616d9c2584cc17d4c18d4084a02e468aba3ddfa33b99ff20125c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227440537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bde036e5899e54ed56fdf1707219cfe67c3634de6c9fe1a139a5b8c9f5235a5`
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
	-	`sha256:e42e49097fe754943ed2309e7c2ac45f6631e5c57fa3daa55479809dc243c87a`  
		Last Modified: Wed, 05 Feb 2025 14:56:54 GMT  
		Size: 64.6 MB (64578222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8928a0cb9d9723d240d99fc6bc7655b62ddf218a866232a1b3789a41992e6757`  
		Last Modified: Mon, 10 Feb 2025 20:26:15 GMT  
		Size: 162.9 MB (162862315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:912af4bdf88bc30de232e87817f4256768d12aafef95e7d7ef624b2099bfe0df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b427a2ff98e82ce97032f9668aa9b96e49d63a47cf5add46fb63fb9905e919`

```dockerfile
```

-	Layers:
	-	`sha256:01bea03a15fdbbc717336bc0d198c316030eb85deea55324c9aed6541a852f2b`  
		Last Modified: Mon, 10 Feb 2025 20:26:11 GMT  
		Size: 5.5 MB (5515690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550e6f7d6914773e12e9e2609be2c9dc17c9cfa9dafc5fefffc6083586de4291`  
		Last Modified: Mon, 10 Feb 2025 20:26:11 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json
