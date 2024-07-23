## `amazoncorretto:17-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:d371bf733322b10e5cf7bd4ca33fd662791bf1629fd3c2f002202f179b48949b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-generic-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:474de9182c2ad22b034b9aac69201bf54463bc915f6f717aa609e5d194ae629f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214863858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c68837846254aedc780c0b0d6124e9c7c9aca0c3d2d5d6cf76a6e18a16312d5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:23:24 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Jul 2024 21:23:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:37766f9d8ddf179208313163dc89d8d39dc16ba3be3bc46534855c244565cdd4`  
		Last Modified: Fri, 12 Jul 2024 13:12:20 GMT  
		Size: 62.6 MB (62649406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e71b596f90da2b1c3adf4fa69754acd74bd35369b6791c2f12a68d3b1f9925`  
		Last Modified: Tue, 23 Jul 2024 00:07:47 GMT  
		Size: 152.2 MB (152214452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6de9647d18e0a8762d76abd4a34968d126d364a4fe997f21948bceb9a63cc8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5538159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c241b5014d1801dee8ba5038287d11ce05102b66a8ec26541a7395a4314c7e`

```dockerfile
```

-	Layers:
	-	`sha256:9cdf32e2893befa2246058cd6515124f0b9b08bc5cdff7e627e99734ea19da7a`  
		Last Modified: Tue, 23 Jul 2024 00:07:44 GMT  
		Size: 5.5 MB (5526938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa376feac22bbd8bcdef42b7f0184f17905806c7c7705b5da179eee33a8d51ac`  
		Last Modified: Tue, 23 Jul 2024 00:07:43 GMT  
		Size: 11.2 KB (11221 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:78829d7ce0df487158dbdfaba50caa0494c3dcb3a7f38a9c14ae4dafd94f1c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215441843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0d17a5dd5ede45b0c050a01f54d90d759a94d883ff3d7720fc188c4e6313d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7670e0f13dba13cacf8a72508b2840f1c1d5b318edb811accb584aab4d61a118`  
		Last Modified: Thu, 18 Jul 2024 22:55:17 GMT  
		Size: 150.9 MB (150866532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:589bc0c33fe26ebac359a44136bb364b3fde9bb030327aeb6a67a38e4214653f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5536991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b922df30415df794d2e8e8bc576bdeb51ffa5d1f374792a64a98d079f87316`

```dockerfile
```

-	Layers:
	-	`sha256:590027cf6c50382cd442fd2fce7b4ac2a48ed7aaa7f040c5e35b650edd50db19`  
		Last Modified: Thu, 18 Jul 2024 22:55:14 GMT  
		Size: 5.5 MB (5525625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f3f7ff7d75762da91b75e8b9c3255450a7ccfa3402c69ed673c182e47fdeff9`  
		Last Modified: Thu, 18 Jul 2024 22:55:14 GMT  
		Size: 11.4 KB (11366 bytes)  
		MIME: application/vnd.in-toto+json
