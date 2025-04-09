## `sapmachine:11-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2eeb8b3ffa5f11c1da44cc0e90beb1b275eece175d205f07b9888733f18501f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:3d39c2f7e2f8fb68fc7663c9dca74e9719578b136bb15d01eb6b119127da805d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79516958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cca522363cf2ac7253e0140a49fe700f9a1c14942b37ada626dcf906260b06`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:19 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:19 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 27 Jan 2025 13:39:19 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de89704ceb7af5cd983f3d60fe5b9b7b56d2153f7110c75c0a4bdb78815db00`  
		Last Modified: Wed, 09 Apr 2025 01:22:07 GMT  
		Size: 50.0 MB (49984593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eb2b2b667c71b8042d4f20bc6adb0e1a8faba381646d8f721ce983549c6a563d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84de7bfffc9e6c72f71c9dc5ad0c66754108244e100d333510802fc611ca3e42`

```dockerfile
```

-	Layers:
	-	`sha256:1a083b8e572917d61e7dd51d958555b8244f3961be812097e54457151a653ec9`  
		Last Modified: Wed, 09 Apr 2025 01:22:07 GMT  
		Size: 2.4 MB (2413476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f347cee15ef29ed94207f19e65efe9b6bfa5aa2ac5fa70207cf0643d9b8de1f`  
		Last Modified: Wed, 09 Apr 2025 01:22:06 GMT  
		Size: 8.8 KB (8820 bytes)  
		MIME: application/vnd.in-toto+json
