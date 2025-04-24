## `amazoncorretto:21-al2-full`

```console
$ docker pull amazoncorretto@sha256:15ab3804c0d0d1202aa7f88a837563d67ec51fb11d55587a21ea6b2bed8ccc84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c42185c35f39a6ba1427470c1a3f7da25552097010ab11b669dce00b14289ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227650078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9d5f87d75ccb80ac7fce3172247614e7a6f285d0d9ed42fe5d3fa5447f72b6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:07f9ec6a4553009171ec20ecdc638afd0eaac432b31f9e1b569f6e4fe9454d93`  
		Last Modified: Mon, 21 Apr 2025 21:48:34 GMT  
		Size: 62.8 MB (62761722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f21cc65f273105f38560a5eb91f93f77cb8ba129a46345ae0845e65aa97147`  
		Last Modified: Thu, 24 Apr 2025 20:08:27 GMT  
		Size: 164.9 MB (164888356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f1d334cd7616a28d4b8d3e67257df199ab994ce9d2ed8b5fd2976e9739d9532b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d02f505c40d2295842f9d7e7f14557c00ab9c7f2eb321b4c8065d0b2aa599ed`

```dockerfile
```

-	Layers:
	-	`sha256:5f25eb2e879a0011918b872bfed0001d5d6a25c01f153d429c94912c66109b9b`  
		Last Modified: Thu, 24 Apr 2025 20:08:21 GMT  
		Size: 5.5 MB (5518903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5017a4ddb617739bd7f36282cd137c23c5a659f8c9ec4273a46a2bab342349df`  
		Last Modified: Thu, 24 Apr 2025 20:08:21 GMT  
		Size: 11.2 KB (11248 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d4646f143c066da2da90bb660d57ba56777ec07300503066a68d3a3f49104c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227488378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30cb6a1d4456d02e6e5ce0bab3aba0a523b5a269b2aa3bfaac8e15a3008c08a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801f2d4c03ced6f3dd698c83d22a792997c6774ac7b281f577007cfc68d4b0d9`  
		Last Modified: Wed, 16 Apr 2025 00:15:56 GMT  
		Size: 162.9 MB (162922556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fb1fbfbd209f89bfdc8c1285606cac711792132c1a045af3b0d4f89a3d24b26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5527114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6a3a39a5c11975f1c6ccbc142c9cb3f35e5d1efd4c0ec071294473f4f31260`

```dockerfile
```

-	Layers:
	-	`sha256:19ae7dc6a140d9125fe1628e723e3f5caf2ac867a7c41d1a580f2d8934bc6557`  
		Last Modified: Wed, 16 Apr 2025 00:15:51 GMT  
		Size: 5.5 MB (5515714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30f2c42519668d4354e365af0af82dcfa2595f1fbb8796818396ff2029ecdca`  
		Last Modified: Wed, 16 Apr 2025 00:15:50 GMT  
		Size: 11.4 KB (11400 bytes)  
		MIME: application/vnd.in-toto+json
