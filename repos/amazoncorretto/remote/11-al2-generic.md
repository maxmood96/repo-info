## `amazoncorretto:11-al2-generic`

```console
$ docker pull amazoncorretto@sha256:9ae9862b94a333f64e7e2374e2581e6692bcf9a8ec55be347822bdbf5d3f52c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-generic` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4e437a0462f5a89ff7399b729c7b8d6e5dc54379681fc5d2f0550f998d385d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.8 MB (210817743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f710145e555e03142d57a170899fd18efe123ce0c6f69fdebaedb5ee74adc55`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0c174e68d4a5429a490fb41eefc2b90cbcfb00c42e691a50f7ccf91b96b339`  
		Last Modified: Sat, 11 Jan 2025 02:29:21 GMT  
		Size: 148.2 MB (148181913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e5f17c5591548d61012a1784b44be654377e3195a9a6728d3fb3313d8e289cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fa8315d0b38ace03abbfd1fe9c291c2968d73767cee866e5fefc607a1177764`

```dockerfile
```

-	Layers:
	-	`sha256:f5edd411674e47161886671a9a85ca79b9e78d8f366689dca34ac7540cb6015f`  
		Last Modified: Sat, 11 Jan 2025 02:29:19 GMT  
		Size: 5.5 MB (5524411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d03963ec9585ce75b6039cd03c0abda80920cca86f0befcf580ade2c28850410`  
		Last Modified: Sat, 11 Jan 2025 02:29:18 GMT  
		Size: 11.3 KB (11255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-generic` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f817640ca23ddb97ec62649d7a8ffb878f163894a41652d71a77d537b3ce87b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.9 MB (209892926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be741bd71646c312df48c6ddf480c8b8d09f3d0bdacfb831d1991df9999d636`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7767988fd4d79438f8a0164f2b7a80d984e37ca965e7dd451e232041b909ab`  
		Last Modified: Thu, 23 Jan 2025 18:34:49 GMT  
		Size: 145.3 MB (145302621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-generic` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a9c50325a3a30de4c2538e94c6b65846f17380cb31382f3b18c50067d9ae3bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5535312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e138dd951c734ac48222e4a3c0c14505862a3b6f3665807f94cf052275fe6c0`

```dockerfile
```

-	Layers:
	-	`sha256:798503de58753814217c0f03e66845393dc5e3e78feb43dd3d29a2b3e23a4d56`  
		Last Modified: Thu, 23 Jan 2025 18:34:46 GMT  
		Size: 5.5 MB (5523905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d233139d79db223bd949c06cad25cf0a7019d7ebe1f70afafef65a1724aac407`  
		Last Modified: Thu, 23 Jan 2025 18:34:46 GMT  
		Size: 11.4 KB (11407 bytes)  
		MIME: application/vnd.in-toto+json
