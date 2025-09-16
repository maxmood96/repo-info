## `sapmachine:11-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:19510612e3cd88be28cfecd9736764d1174afbe905bf21ffc07771d078a6b14e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:18b66f7c8a85198575eb442eecd69d52f17fd300018e771b100a88e5c7dafd3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80118987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75100bfbd550915200bb3782d2ce81099e3ef32ab8a0e327c9edeca4d025e29f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:16 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:16 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1d593c923882e938ecef0d3e8d196e1ab2edb46867af1cebd167e4ad534000`  
		Last Modified: Mon, 15 Sep 2025 22:28:41 GMT  
		Size: 50.4 MB (50395537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2150962a139a224932f056d3e3929577c127976ea4107f2a1804be32053d1ac2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c0b23635ece1b809e016e5e0164293daa506677b43ed383e2f7d369f8a2f82`

```dockerfile
```

-	Layers:
	-	`sha256:b9847062bc62a2d4fdfe983be3d3e4e9268f7a8e219b95bfd8a2056f0f8e4fd5`  
		Last Modified: Tue, 16 Sep 2025 00:04:39 GMT  
		Size: 2.5 MB (2523633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67ba21427abbe44b9618f01bef6b7c793a2c8363d538743ca57499e11db8a70f`  
		Last Modified: Tue, 16 Sep 2025 00:04:40 GMT  
		Size: 10.1 KB (10092 bytes)  
		MIME: application/vnd.in-toto+json
