## `sapmachine:11-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:159a8ec98f64468138c4ed709120db52396e1d1d8b87e8f42fcf26366f0b454a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:c55c420be9d305540ab3a979b6c66d9e823188bcdbaa1f375816ccf846d207bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79800172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b62ab27deea503b9cec38327460c066b13ac6234b0c0dcba27a8e3e3af9ae4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Jan 2026 05:37:25 GMT
ARG RELEASE
# Tue, 13 Jan 2026 05:37:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Jan 2026 05:37:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 13 Jan 2026 05:37:27 GMT
ADD file:3077ee44db3cc7d38740d60a05c81418dd3825a007db473658464f52689e867b in / 
# Tue, 13 Jan 2026 05:37:27 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:46:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:46:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 15 Jan 2026 22:46:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a3629ac5b9f4680dc2032439ff2354e73b06aecc2e68f0035a2d7c001c8b4114`  
		Last Modified: Tue, 13 Jan 2026 07:03:32 GMT  
		Size: 29.7 MB (29726011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40fa357dad078ce1eef1bf75520b048bae90d872a34cd46cf0c9bd3674de613`  
		Last Modified: Thu, 15 Jan 2026 22:47:08 GMT  
		Size: 50.1 MB (50074161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d79f09d1e8e947c9ead3ec0089df2c8f15224972812bd56a8bfd6a0a6974e617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f969038823190265b2e8962fbaabb316ab671b31e490dec3799ad2e5f534ab70`

```dockerfile
```

-	Layers:
	-	`sha256:faef1abee3e07371320fcf7b3b476ee3be65519bad6468ac8f5f074bc0c5f665`  
		Last Modified: Thu, 15 Jan 2026 22:46:54 GMT  
		Size: 2.5 MB (2523645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55ae548c89af5eb5818718d9b87a0d945270c360e6163783a94cd98a7385c2c3`  
		Last Modified: Thu, 15 Jan 2026 22:46:54 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json
