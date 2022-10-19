## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:8cac064ac11e626b124f0d081dd7f85c17d0925e1c2ef768ca5c98bbb58d8007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:4bc993088086c4c245942726371ce3cf38bab56883f0dd7e1ff6f30c60ec6fce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242921163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510d8bb401632ac2a260973d4f4a8f75d616fb4bca9ec6b4f5342c44cbb309f2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 04 Oct 2022 23:35:12 GMT
ADD file:8faed18d471598732aa3816c8f70e227f16f4de5db6c5c32812a09141048f56d in / 
# Tue, 04 Oct 2022 23:35:12 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 18:09:12 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:38 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.1     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Oct 2022 19:48:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 19 Oct 2022 19:48:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb0b3276a519f5e7085f51c75989b287b234b3508e1524cf2cdcbc397c06ec3d`  
		Last Modified: Thu, 22 Sep 2022 20:37:52 GMT  
		Size: 28.6 MB (28574451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf0b13da87099833442bbfa96ea98ecb8c17f08743ed487859d5091012fa27a9`  
		Last Modified: Wed, 05 Oct 2022 18:11:18 GMT  
		Size: 7.9 MB (7920113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994bdc4c603a252d3d427fbb2731f10f2ec4c2e382c5f95faaf78893e034a95f`  
		Last Modified: Wed, 19 Oct 2022 19:50:00 GMT  
		Size: 206.4 MB (206426599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
