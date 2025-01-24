## `amazoncorretto:17-al2-full`

```console
$ docker pull amazoncorretto@sha256:1d4c15a86d35ad5115506f9d38f471e8b2c3921e221996702d043bcf5a0d4bc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:98f21381101889c352e76f68780e40ff7951ba247e0e86f0b7dbfcaf27aa3d99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.3 MB (214267621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b019d000279cfc104afb49179a0151c026da3bbd9e644287e335eb5eabc3853e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:24 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd579850bf0242e650f949e761feb5ab62b7fe7b418c7fe67a1c9ebd5e97619b`  
		Last Modified: Thu, 23 Jan 2025 18:27:31 GMT  
		Size: 151.6 MB (151631791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:10d7f29396c224e9c5863c6b3fa5cebeae28b66c38f3045edbf8250b97e1ece5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cfbc54f1683a3e6828a75dfae60b2fee40698509e052091ec0a0bfa9544630`

```dockerfile
```

-	Layers:
	-	`sha256:85ba947d46de55c0c51e7703cbed114398e93454242ea2a68aa2b15f7c58739d`  
		Last Modified: Thu, 23 Jan 2025 18:27:29 GMT  
		Size: 5.5 MB (5517106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa3018c63decb09dd0d4f51ef26427967fbc2081728104d3fbfbe20b7dab1115`  
		Last Modified: Thu, 23 Jan 2025 18:27:29 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a72df4e6791618b75b3e5f06097401a687ea5e1ad069ddbd9a735379317f72e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214905497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5e4e9f9debf69ce8fdbdeccf39556b779556877bb2ded0f438a2c22f4c5276`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b396860cb9f9c27bdb6b1b3bf0882bcb2815907fe44d9d85f398239e98a1602`  
		Last Modified: Thu, 23 Jan 2025 18:41:53 GMT  
		Size: 150.3 MB (150315192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0c5ab719f28b8f9cdeab138832cc58f85daa57d06946986a2bc295f0ea4d9867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a905cacbfb408b7becf73e270b6e2d0a0832928e4ab2c4104144f7f5c83e9a3`

```dockerfile
```

-	Layers:
	-	`sha256:c67d8d5f13ab8bcc981ca1fff736627c73374ea738682019da1b0f93ca53f8c4`  
		Last Modified: Thu, 23 Jan 2025 18:41:49 GMT  
		Size: 5.5 MB (5515795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf91283e0932dab026b0163a27b8ab21a8356052394040e90a9390e752264b9`  
		Last Modified: Thu, 23 Jan 2025 18:41:49 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
