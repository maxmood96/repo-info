## `sapmachine:26-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:4cfd9176d328b8a5c5aea999c8e775c45cef955c4d53e19bfe4e8172dcca0d55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:26d27c05c74eb89b115f83cb4b45b3e4f9c89da8fffcce976dddd5beffa29726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255718978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995336f21665244c5ecd7f6488e00e8aff34c7fa5ce000587e52cf780528a1fb`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:52 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Fri, 15 May 2026 21:20:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918043abf09f37e12ccf43d4dd79c4046a7ad29b9204ffae03ca820942a5fd76`  
		Last Modified: Fri, 15 May 2026 21:21:14 GMT  
		Size: 226.0 MB (225982294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7309344e853021a4faa04482cc78208ebd8d1eddbacdfd0fb55b4483d9fa0cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2632326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505c6dd77913073e607841cb3bff6908f71f8f153d56c0c43df30cc9dec253b9`

```dockerfile
```

-	Layers:
	-	`sha256:908c3d310a5507feb31eb63d99dfaaf64956d03fcee12af7fc3ed6946210ea18`  
		Last Modified: Fri, 15 May 2026 21:21:09 GMT  
		Size: 2.6 MB (2620957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0737a60ab8de30e093cdb21a10b87962077340bb657236aeedb29ac4bee7c7e`  
		Last Modified: Fri, 15 May 2026 21:21:09 GMT  
		Size: 11.4 KB (11369 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1fc8d6c42b20f862fe39c380edc9f3b4e2c6f799f63fd912ae3b825c0f9aeadd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251419980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266348d31421c411eb952bab4ed16c04a2a94faf2702cab017faf719f8c139a9`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:21:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Fri, 15 May 2026 21:21:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57f4b0c2d920a1332f9522844b184eeeb7eef0ca730b2da6d1bfb9e75208855`  
		Last Modified: Fri, 15 May 2026 21:21:31 GMT  
		Size: 223.8 MB (223813357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:644567df798fad52e6d33dcfb892586b2675439d5c41da4fbbc76b2628355c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2632302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1768c918b2c72b3da20fe04d85e66aca30ed10f37c0b8cb16bfd0fc761509b76`

```dockerfile
```

-	Layers:
	-	`sha256:f2cd2e696b2757451b5872b2b8285d7f12fc6e2cc14c6560ab78b26e42df3746`  
		Last Modified: Fri, 15 May 2026 21:21:26 GMT  
		Size: 2.6 MB (2620732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0563d240ab5b86b41a854352faccd132509bbb8a93ebceedf1bab8f53a087dfb`  
		Last Modified: Fri, 15 May 2026 21:21:26 GMT  
		Size: 11.6 KB (11570 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1a48a2b7c7ca6a2f0d981facc89a6274dbf8b3f8361612471a8f423f7c9f3635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261809549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5c40003de15b47cb4c0da4978a786feaf7f9e174c790b9312ed9991ca81c54`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:33:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:33:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Fri, 15 May 2026 21:33:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3db6f841dc77addf3e76849feb07ed01fc44e52c9229091e5a464f9abbcf21e`  
		Last Modified: Fri, 15 May 2026 21:33:48 GMT  
		Size: 227.2 MB (227162829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:76d550389a3682627ed9f4eb3e7d4c406e9071d03995bf6d08afa3b10b608009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a86dbd57855c4fc6424c465e0c0ac53ebb1a9cd379fe2e7cb1ecc252b63885`

```dockerfile
```

-	Layers:
	-	`sha256:eadebd09bd2f3631229561ae2edcf64a4b13c05b986fa00d6697f80ff0c84cd4`  
		Last Modified: Fri, 15 May 2026 21:33:43 GMT  
		Size: 2.6 MB (2617973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1491058370a08e7de437eb2e8ff58cb13d4d467fd6f2c9ddfcf12387757929`  
		Last Modified: Fri, 15 May 2026 21:33:43 GMT  
		Size: 11.5 KB (11462 bytes)  
		MIME: application/vnd.in-toto+json
