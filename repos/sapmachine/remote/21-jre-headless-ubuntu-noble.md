## `sapmachine:21-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:a7d3408f80d1fde9a84b1a33971420903878fbe2ed8041aeb34625b5ae252c36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:5ec8d7bd62f114a3e5339e4c509cf099cc048e134f26dda57cb0f2692db79ab3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88649097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:639dcf4ff223d86049942c6b791b0e8886b7d59ff5dacef979776eeba774cfc7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a51e2c6363f017e14332ffcd08e848beca8083072841ecf20a866517754672`  
		Last Modified: Wed, 09 Apr 2025 01:20:51 GMT  
		Size: 58.9 MB (58931445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c95e917a0b0f4f05bd8a84302146285f7010085913dadc84642d17a6a8de60c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fbbc837d6299a4ab7df0bfb73358575465427e6b7dc9c2209eb4e9eb73727b`

```dockerfile
```

-	Layers:
	-	`sha256:9b798d973688af32c42c4288f0e0643f289917b75b16afadb2e46485d73b1dce`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 2.2 MB (2150984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff3a1168323c89a14ef04c03437e86f3f85da6e9fa8524d784ea926d44391f9`  
		Last Modified: Wed, 09 Apr 2025 01:20:49 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2d5b7f0e4864f666c55252c3c628a7e8cb114ca2c59b5f6da855554ac8568008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87002258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:125219cf995adf45e9dc6f53928f633c76ee1655507523f9c47a0e850b917bcf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57173018c7ed45d0383d6311c2dbb906f5246b6005fb0bab06718953aa7bd0f1`  
		Last Modified: Tue, 04 Feb 2025 15:28:31 GMT  
		Size: 58.1 MB (58108660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0b6594defd81c5f9bc0d28480562f676ff01443a65fe455bc5d3dc71a2dafc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed569643fa1195de8363c305e71fa328452e33fea63593f5e56b767999a7d825`

```dockerfile
```

-	Layers:
	-	`sha256:52940923d476da8b0a2a52f5b61388a3bb60426ab89e8fa63a342d249e161192`  
		Last Modified: Tue, 04 Feb 2025 15:28:30 GMT  
		Size: 2.2 MB (2153722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:970bad296000ebae4a46c587d002d21472be10d193fb2f425a02f995b2d8d9b0`  
		Last Modified: Tue, 04 Feb 2025 15:28:29 GMT  
		Size: 10.8 KB (10815 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4cc53de9f8201c7ac4ebe5667ccec04fbaf66aeaa7d2d1cbf416bcd0ac507fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94763918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deed17b87d4e826c75b9e787fe19731a00bb2dd4c26fdb2955bf6ab7198d41f2`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:13 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:13 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb2bcec50d88d52f7d182a9b7045444c61fdd468c6c4fe8292fb5c154907797`  
		Last Modified: Wed, 09 Apr 2025 06:56:03 GMT  
		Size: 60.4 MB (60423051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3e3a4b4b472f6e8731afb22c1e858365dd5b73b84e3e131ce33ae9eaaa2f2c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ba66151e588d499ba62c6c321ffad47bcf5ff4611cb5385b455628959e0ea3`

```dockerfile
```

-	Layers:
	-	`sha256:285f68eb682d2169aef142d12b6695f94ca313ca572c234b542dad03318ef1d2`  
		Last Modified: Wed, 09 Apr 2025 06:56:01 GMT  
		Size: 2.2 MB (2154890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af169d75925ecb84f4459d24588cdac248311e2170a192991340af52fcdbdb6c`  
		Last Modified: Wed, 09 Apr 2025 06:56:00 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json
