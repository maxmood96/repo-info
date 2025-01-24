## `amazoncorretto:latest`

```console
$ docker pull amazoncorretto@sha256:0194fab69fe3579eca0cbadadeaf922c11171d479eea006930809395eb196038
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:latest` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9b5a651f8a82b7fc8d3e03942d1823fd339e4823037b97db80bae83738810816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138240622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77f891e61290a19c214970c67d34f10983e918339b54b4dfc502e1aa1721fb0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 22:08:39 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 22:08:39 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=1.8.0_442.b06-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2ddc0aa2636ed19b988b4176374929a92f5862f6c6e88ea255d352140af781e6`  
		Last Modified: Fri, 17 Jan 2025 20:13:56 GMT  
		Size: 62.6 MB (62648554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857466e9d40e7d7de6e3e5fa7d4f2af30505a7d901e19a6df289cbce9d57ba75`  
		Last Modified: Thu, 23 Jan 2025 23:07:57 GMT  
		Size: 75.6 MB (75592068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:32aba517ee89a7ae6a19561ed5b5d75de0d562b73deb02a84b68e96890b0ca68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ca86657fbf8b54835044c606cba757840ac2ed9b0402817b98fe7cf417ed9a`

```dockerfile
```

-	Layers:
	-	`sha256:9eb37d70a187ce6f9ef3fc94923217d6bc42ed16b17db09129af47d3b0df5c07`  
		Last Modified: Thu, 23 Jan 2025 23:07:56 GMT  
		Size: 5.4 MB (5359564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ef433621eb94a526a435ad425698e142ee53418ed8c3228ca03a47c1a230ba1`  
		Last Modified: Thu, 23 Jan 2025 23:07:56 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:latest` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c3c9daf92de5ec4dd3015e8b83b163444b368de2c700e4aaf29fe9bdb4773f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124261572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d08b269d9e2857804877dbdd126a0ed04b95e30744419bcd4330c531e64f99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 22:08:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 22:08:43 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=1.8.0_442.b06-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:dc3d403853487343f06bffefe21e65d842f88da2d7a1073ba2820fdb1b7ece72`  
		Last Modified: Fri, 17 Jan 2025 20:14:11 GMT  
		Size: 64.6 MB (64590432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f60d3a27242629037dafdbc0af3eeee6045ae663cafb36f1e43b48efbe4fd5`  
		Last Modified: Thu, 23 Jan 2025 23:07:53 GMT  
		Size: 59.7 MB (59671140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:latest` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:af9ee00e6d0f4eaa0bb2f7659bf9b8ed6ecaa355206dc3f4a0eed6a08a8e37d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c704b13a006ad4a638b19ae765fbdd32aba74581c46fd23cf912ecad68f029b`

```dockerfile
```

-	Layers:
	-	`sha256:884c5f3d083e8033623454cbf3948ce86d9c776aa308c433a0b52c963ce12cd3`  
		Last Modified: Thu, 23 Jan 2025 23:07:51 GMT  
		Size: 5.3 MB (5338063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827d798233feab1fa4e5bfd2a18d6d38f9ac1402dbee7a37a589085aa8f9a3dd`  
		Last Modified: Thu, 23 Jan 2025 23:07:51 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
