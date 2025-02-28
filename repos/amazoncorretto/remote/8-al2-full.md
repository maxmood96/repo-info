## `amazoncorretto:8-al2-full`

```console
$ docker pull amazoncorretto@sha256:138d0ba65c8bd4b920dd62ed99177b004096196f56da9cddeef925f518732d1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cc406ded155885da5da53b67cfb05b9c27794663d3dfc656c20d6f9ea03c04c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138459146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0defdde877065aebd9a81445928dad3b7c407e1b2bdf4f8363a75d8643cdadb`
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
	-	`sha256:7f0a890370e7b6290884eb8b70dcfcd6749f097764b13db947cdd9196f5b6ecd`  
		Last Modified: Wed, 26 Feb 2025 15:57:24 GMT  
		Size: 62.8 MB (62802042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3987d930614bff608d3dd8c33d6c69acaed62e7d377df635ae7526a7136c5770`  
		Last Modified: Thu, 27 Feb 2025 21:07:59 GMT  
		Size: 75.7 MB (75657104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:20527fdbe04ee0dc48ed84ce5e7586c25f46f5afefa0cc9d9dbc71b7f2932a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5371138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32287c58bc5940618194dfa1e681e2a41b0a2183a452815d4ecbfb4a74a3a8dc`

```dockerfile
```

-	Layers:
	-	`sha256:1b38ecb9f4ab2cbdbcf418499ec0896fb95fdeb8ba74d4c30f0b5632690e715b`  
		Last Modified: Thu, 27 Feb 2025 21:07:58 GMT  
		Size: 5.4 MB (5359568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5299de74f2c9baa6156475c19e797d04648738711d86ab11614b9419e183be0`  
		Last Modified: Thu, 27 Feb 2025 21:07:58 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b0f776d2995d39b11efdf45ec96f54dba1aaef3e1e2e1b8a019820f2a6977bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.1 MB (124131950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaa1d844fb84015d42c9d3de8d502a0d04f3c705f2c585f9e56bcb60dc28dd3`
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
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2385f120b7c583c3e8c6734b7c5715f966f96e99c44472b350d802223c20ea6b`  
		Last Modified: Thu, 27 Feb 2025 21:07:53 GMT  
		Size: 59.6 MB (59610742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c9192c56728789b459820824c688af238cbdaa553020bf2bc5bf2f0382830938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5349801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae582369786bf202e133977c2693598b8ca256e166ff1fea509c73162658e38`

```dockerfile
```

-	Layers:
	-	`sha256:cb83189959c6e81128d06ddfe75edce0c88d2db85764d30bb3b0ad45f934158e`  
		Last Modified: Thu, 27 Feb 2025 21:07:52 GMT  
		Size: 5.3 MB (5338067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:553316ff4ec22329f0a7b7f3d00ba6faf58b58d77d9f8c050720f441e1813f4f`  
		Last Modified: Thu, 27 Feb 2025 21:07:51 GMT  
		Size: 11.7 KB (11734 bytes)  
		MIME: application/vnd.in-toto+json
