## `sapmachine:11-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:53428bbc1d8b29edaa4b92a56f8138e9e86a0e52f1c2e02c022a2639af9fa25e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:63cf2e58a51cfd2308f240f0593c044f54dbe118864e371a382646aa6497b0fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230424770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05f2bf7fe388f966d9ff1e87500ac9bac3ed42dfd777a7e602b5c46eac10c0b4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:26:02 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:26:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 17 Mar 2026 02:26:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a36b8f28c763c55de73ab40f32f8708ac2b9f31e568b6103812d9a7da75f32c`  
		Last Modified: Tue, 17 Mar 2026 02:26:24 GMT  
		Size: 200.7 MB (200692777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2214c44879a49f355ea0d35b5e91ed0c5496194b0642b551ae2be1630def1d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b535814306059c907c5ffe3e93222a08429037c326c04f43faa034d25c1c49ff`

```dockerfile
```

-	Layers:
	-	`sha256:cdc2af1fd459fa4eece636155e13a136bbcc4aab6d3d47ac6c96f1771d2b2ea8`  
		Last Modified: Tue, 17 Mar 2026 02:26:20 GMT  
		Size: 2.6 MB (2615642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4821362c3ca260ecb26d47ddb8adc94625f005fbf64c7039e8f62a45e2cc4143`  
		Last Modified: Tue, 17 Mar 2026 02:26:19 GMT  
		Size: 12.6 KB (12607 bytes)  
		MIME: application/vnd.in-toto+json
