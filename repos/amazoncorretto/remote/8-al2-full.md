## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:5eec9b964b27e7f8ae6a8435212de928349eeb03ec4ff4b080d85100d36c82e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:89bcded3505da426236bb62155a26c85b8bb04277439e0f992a80b6e333103bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138188921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dd7d26f1d5555b1e44968033d73333974bf23bee52c678e4e0ae68138ff5a5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:19:55 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Fri, 28 Jun 2024 00:19:56 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df879df5a13963c139628f4d5cb7084cdf55c3b07deb2261c943aac199ccd617`  
		Last Modified: Thu, 18 Jul 2024 00:55:53 GMT  
		Size: 75.5 MB (75542283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:411ae5b28a35f05ce6f002aadf20503e745c1142fef657d36972c6f3a3f2e9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5381005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ba49fbde416f176a345e4a4e6ac9feb0f40e2d815c572d5f89e43e18615e04`

```dockerfile
```

-	Layers:
	-	`sha256:3f2037ce3e052b8ed07c71b1ca6be6335ed6b0836b2319012b4eb70b2ab5be54`  
		Last Modified: Thu, 18 Jul 2024 00:55:52 GMT  
		Size: 5.4 MB (5369674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e0b3b70c97fdbfeef09662b4baf3416e6f4392e2fdbd130f909ab9a96317fc5`  
		Last Modified: Thu, 18 Jul 2024 00:55:52 GMT  
		Size: 11.3 KB (11331 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:90e2a0a20c7c29ae7b5de60e23751c4f76ae1fab589ae14f9e6ca2036b6c845b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124224727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60bcd9e835387a2439fac54a14cf44ee65e294291f19628538fd63aee5d82f61`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:40:02 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Fri, 28 Jun 2024 00:40:03 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc38a326f1fffaeefd7e2ea5affa71e5743284a4823cbfe077e2994b97ba730`  
		Last Modified: Thu, 18 Jul 2024 00:55:37 GMT  
		Size: 59.7 MB (59655962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3b80b8368d248c2881a7478eeedaabbf26eb656310a0cce9046cf0db1cc2bf46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5359914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81a56dbaac66a54e10382d4c763f3873f02a483dc5fb6b0f96041fa4803efcc`

```dockerfile
```

-	Layers:
	-	`sha256:810aef257c70d9c364cbdebd1c723884cdf0c8d93b879418c21c0af2cfa9cc53`  
		Last Modified: Thu, 18 Jul 2024 00:55:35 GMT  
		Size: 5.3 MB (5348221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0544a0208b0b411db10b86ee11f8d9f265c0a8cbfc9c5a475453340948f25fbf`  
		Last Modified: Thu, 18 Jul 2024 00:55:35 GMT  
		Size: 11.7 KB (11693 bytes)  
		MIME: application/vnd.in-toto+json
