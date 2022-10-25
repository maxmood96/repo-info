## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:11c419071f4f3dfa12ac0a5f30d247f3b6ee3afe6059b0245e8a4f29c43faca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:eabf7cb4a8fd422a420b66c5cdd1fe752d05c8571c2e4b9732aa3c3af806a430
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242928424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a254b5a16cccdd9a7eaf300efe1e5b6684957f8f7f72ec386b2bd8aaabaf45b3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:28:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:30:30 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19.0.1     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:30:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Tue, 25 Oct 2022 18:30:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce68e21cf06ac72066ade930bdfb3d7e3b9da0cc4d6d121a841d01b83627b971`  
		Last Modified: Tue, 25 Oct 2022 18:30:47 GMT  
		Size: 7.9 MB (7923897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca35af67b8ae54cc263628b481d690ad427e09b66ed471aac8c5941ffbae20e`  
		Last Modified: Tue, 25 Oct 2022 18:31:53 GMT  
		Size: 206.4 MB (206426693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
