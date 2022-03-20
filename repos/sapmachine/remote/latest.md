## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:a6db65f918fdbf1d4866bb75f90a3be36b34a2509d02480c9e89904e52dc4a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:75ec906b3487f392bc63a7d41a07868bcaed475c1508e70cae4503299136d4f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234531362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75c523745a311f939b2ae43b05c80168474efa5d18bf72f50ba76cbb873de10`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 23:22:58 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 23:23:58 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.2     && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 23:23:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Sat, 19 Mar 2022 23:23:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91055c9c019f595bbb97432167e9b8a8ee3df50484deed23fbe2a4357d9d20e`  
		Last Modified: Sat, 19 Mar 2022 23:24:17 GMT  
		Size: 8.3 MB (8317733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d265f2ccb1a96bf885c42ae6a77edc663333df3790ca1dcee2a00f703a44de5`  
		Last Modified: Sat, 19 Mar 2022 23:24:55 GMT  
		Size: 197.6 MB (197647720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
