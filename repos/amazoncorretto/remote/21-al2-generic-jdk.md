## `amazoncorretto:21-al2-generic-jdk`

```console
$ docker pull amazoncorretto@sha256:11f468c4df18268a3a7fc292e24d283d0a818a01ec9b7da2b34c46d1f7cf0378
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2-generic-jdk` - linux; amd64

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

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

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

### `amazoncorretto:21-al2-generic-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4a379a1cddb2268df7f9ae8f07e5a0918bcf49d238e6e28c5125c771fba3a008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227494177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff83b8445bccef1864db8d7ad25ba82f1e53091957dc493e58b44b49c5387d5`
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
	-	`sha256:928bddcbf112315a029f894cf829df2ae1b28c89ecaa6c142e3d47e62c803337`  
		Last Modified: Mon, 21 Apr 2025 21:48:49 GMT  
		Size: 64.6 MB (64582610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98cbb4a560178f2ead50defe7c83046465030811972097927386c0144488eca`  
		Last Modified: Thu, 24 Apr 2025 21:21:33 GMT  
		Size: 162.9 MB (162911567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2-generic-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f4e4c90358ae9ad73470464d2cf8b19016a7074eb74bcb1796764c473f8d7f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5528991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab6ffd0eec3bf909b57625647d967b57053f9ddce8cc8e37cf97a4789af5aaf`

```dockerfile
```

-	Layers:
	-	`sha256:8f36deb8acf92885fd1e244657c1f9df15acf73a941279e4fc552bb7d452e46a`  
		Last Modified: Thu, 24 Apr 2025 21:21:30 GMT  
		Size: 5.5 MB (5517592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:908b30af6d7efd069552c7c29478a20fc331096b47267da5eb2501958066bfda`  
		Last Modified: Thu, 24 Apr 2025 21:21:29 GMT  
		Size: 11.4 KB (11399 bytes)  
		MIME: application/vnd.in-toto+json
