## `sapmachine:11-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:74589a21f4c7d1efa41c81ee9faa431001a1c669726180f9e8eaddaf2da0918a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:d54060769d07dd06c77fae35bb06f3574e198bae457732ab2d142b6a607c867a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80118717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90953f7a6fba3c2c9370530e3d053c11fb062a9b98f7f03fe276ce257ea62dd6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:39 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:39 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:39 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Mon, 11 Aug 2025 06:09:39 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:39 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 11 Aug 2025 06:09:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e829dea88b63aa11c140c1c3d43b05aa2f4ee4ed2caf3e7b4a2e49535f070b3b`  
		Last Modified: Thu, 09 Oct 2025 21:28:08 GMT  
		Size: 50.4 MB (50395570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b29338f53b1fe4de22f3042ecb5859079d7a35b4ce1a2b52d2262af3980c68be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74689f5cb620554888cc73524024039c5cf0e54e1d69bfc849975d7846d320d`

```dockerfile
```

-	Layers:
	-	`sha256:9926943c7817126db7232e9de9c9afbf086ba9f283499a4ebfcee37f55eaf8c1`  
		Last Modified: Fri, 10 Oct 2025 00:04:39 GMT  
		Size: 2.5 MB (2523633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42be247444bcb216f53aef385ceec7e76c74780f45e355ad65f269c5f2b1ec10`  
		Last Modified: Fri, 10 Oct 2025 00:04:40 GMT  
		Size: 10.1 KB (10089 bytes)  
		MIME: application/vnd.in-toto+json
