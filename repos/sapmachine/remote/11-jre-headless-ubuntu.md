## `sapmachine:11-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:d321c0b2c0487f8063ceff176c6b51e0d2fcea9045b67dd79980bf3e83a5113a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:c6dc8e63b15f782d02660a19fe5da92d34b65c05d2533263a2ac963b4538a093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78609310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd4907a4e6cb16b3eb6dc528ea5755df9e94a1eaf17db2b1e16f01cef2fdc74`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 13:01:35 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:01:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:01:35 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:01:37 GMT
ADD file:249778a1782b02a1c2bcf9f292f5778d81442a53c3de1958d712f10baf7e0b60 in / 
# Wed, 01 Oct 2025 13:01:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 21 Oct 2025 21:30:25 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4b3ffd8ccb5201a0fc03585952effb4ed2d1ea5e704d2e7330212fb8b16c86a3`  
		Last Modified: Wed, 01 Oct 2025 15:21:59 GMT  
		Size: 29.7 MB (29723147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c044e8e4680e2ef1a621878c70bc2b8eb0c6234c136a2c79fbe4aa05259b973`  
		Last Modified: Wed, 22 Oct 2025 02:45:03 GMT  
		Size: 48.9 MB (48886163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d30fe715b8efc64880c23411f7b78a85e05a39829e877510e58c0b1abf4b779c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8021680eff8d54b5b34eff8443ca0cf55d0712fd34ea6cefb95a4ba72ad0a53f`

```dockerfile
```

-	Layers:
	-	`sha256:fd825a8618ec36d9372ac7e206614a9826a407142ada9b3173a65bdc5ab57b0a`  
		Last Modified: Wed, 22 Oct 2025 06:04:52 GMT  
		Size: 2.3 MB (2277811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d50b379fc6001cc22c3b764f1ed60be97eeb35e8649058df2d3441262e6d54b7`  
		Last Modified: Wed, 22 Oct 2025 06:04:53 GMT  
		Size: 10.3 KB (10272 bytes)  
		MIME: application/vnd.in-toto+json
